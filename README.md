# Explorando-os-Recursos-de-IA-Generativa-com-Copilot-e-OpenAI
Desafio DIO para testar as funcionalidades do Azure

Para utilizar o Microsoft Copilot:
1. Abra o link copilot.microsoft.com e faça login com sua conta pessoal da Microsoft;
2. Na parte inferior da tela, você verá uma janela "Pergunte-me qualquer coisa".

Teste alguns exemplos. Pergunte quais são os pontos pró e contra de se viajar no inverno.
Você pode pedir para ele incrementar a resposta. Diga a ele para te apresentar mais três motivos pró.

Experimente a geração de imagens
1. Digite no prompt: Crie uma imagem de um elefate comendo um hambúrguer.
Obs.: Na resposta, há um texto na parte inferior que diz "Powered by DALL-E". DALL-E é o modelo que cria imagens a partir de linguagem natural.

Experimente a geração de código
1. Digite no prompt: Use Python para criar uma lista;
2. Digite em seguida: Transcreva para C#.


Explore o Azure OpenAI
São utilizados os modelos generativos de IA desenvolvidos pela OpenAI para a plataforma Azure.

Para prosseguir com as atividades, você precisará de uma assinatura do Azure aprovada para acesso ao serviço Azure OpenAI.
1. Para se inscrever para uma assinatura gratuita do Azure, visite: https://azure.microsoft.com/free;
2. Para solicitar acesso ao serviço Azure OpenAI, visite https://aka.ms/oaiapply.

Provisionar um recurso Azure OpenAI
Antes de utilizar os modelos, crie uma recurso Azure OpenAI:
1. Entre no portal do Azure (https://portal.azure.com/);
2. Crie um recurso Azure OpenAI com as seguintes configurações:
   a. Assinatura: uma assinatura Azure aprovada;
   b. Grupo de recursos: escolha um grupo de recursos existente ou crie um;
   c. Região: Leste dos EUA;
   d. Nome: um nome exclusivo de sua escolha;
   e. Nível de preços: Padrão S0.
3. Aguarde a conclusão da implantação.

Explore o Azure OpenAI Studio
1. Na página Visão Geral do seu recurso Azure OpenAI, utilize o botão Explorar para abrir o Azure OpenAI Studio numa nova aba do navegador. Como alternativa, navegue até o Azure OpenAI Studio (https://oai.azure.com/);
   ![image](https://github.com/ThiagoMouraP/Explorando-os-Recursos-de-IA-Generativa-com-Copilot-e-OpenAI/assets/43223265/d7e4884b-20f7-479f-8090-2ba99aa1354c)
2. Veja as páginas no painel à esquerda.

Implantar um modelo para geração de lingaguem
1. Na página Modelos, veja os modelos disponíveis na sua instância de serviço Azure OpenAI;
2. Selecione qualquer um dos modelos gpt-35-turbo para os quais o status Implantável é Sim e selecione Implantar:
   ![image](https://github.com/ThiagoMouraP/Explorando-os-Recursos-de-IA-Generativa-com-Copilot-e-OpenAI/assets/43223265/5bd1737e-a45b-4cf0-9f9f-71cb6add9e31)
3. Crie uma nova implantação com as seguintes configurações:
    Modelo : gpt-35-turbo
    Versão do modelo : atualização automática para padrão
    Nome da implantação : um nome exclusivo para a implantação do seu modelo
    Opções avançadas
        Filtro de conteúdo : padrão
        Tipo de implantação : Padrão
        Limite de taxa de tokens por minuto : 5K*
        Habilitar cota dinâmica : Habilitado

Use o playground do Chat para trabalhar com o modelo
Agora que implementou um modelo, você pode usá-lo no playground do Chat para gerar saída em linguagem natural a partir de prompts enviados em uma interface de chat.
1. No Azure OpenAI Studio , navegue até o playground do Chat no painel esquerdo.
    O playground do Chat fornece uma interface de chatbot com a qual você pode interagir com seu modelo implantado, conforme mostrado aqui:
   ![image](https://github.com/ThiagoMouraP/Explorando-os-Recursos-de-IA-Generativa-com-Copilot-e-OpenAI/assets/43223265/d8fa3d35-e9ae-4c8a-aecc-ed313b3c8b52)
2. No painel Configuração , certifique-se de que a implantação do seu modelo esteja selecionada.
3. No painel de configuração do Assistente , selecione o modelo de mensagem do sistema padrão e visualize a mensagem do sistema que esse modelo cria. A mensagem do sistema define como o modelo se comportará na sua sessão de chat.
4. Na seção Sessão de bate-papo , insira a seguinte mensagem do usuário:
   What is generative AI?
5. Observe o resultado retornado pelo modelo, que deve fornecer uma definição de IA generativa.
6. Insira a seguinte mensagem do usuário como pergunta de acompanhamento:
   What are three benefits it provides?
