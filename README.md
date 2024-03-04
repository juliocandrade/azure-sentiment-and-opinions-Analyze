# Análise de Sentimentos com Language Studio no Azure AI

Para a realização do trabalho, foram seguidos os passos descritos no site **[Microsoft Learn](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/06-text-analysis.html)**

O Processamento de Linguagem Natural (PNL) é um ramo da IA ​​que lida com a linguagem escrita e falada. Você pode usar a PNL para construir soluções que extraiam significado semântico de texto ou fala, ou que formulem respostas significativas em linguagem natural.

# Uso

Criar um recurso de *idioma*, configurar o seu recurso Azure AI Language Studio, Analise das avaliações no Language Studio.

# Processo

<details>
<summary>Crie um recurso de *idioma*</summary>

Você pode usar muitos recursos do Azure AI Language com um recurso **de idioma ou de serviços do Azure AI**. Existem alguns casos em que apenas um recurso Idioma pode ser usado. Para o exercício abaixo, utilizaremos um recurso **Linguagem**. Se ainda não o fez, crie um recurso **de idioma** na sua assinatura do Azure.

1. Em outra guia do navegador, abra o portal do Azure em https://portal.azure.com, entrando com a conta da Microsoft associada à sua assinatura do Azure.

2. Clique no botão **+Criar um recurso** e pesquise *Serviço de idioma*. Selecione **criar** um plano de **serviço de idiomas**. Você será levado a uma página para **selecionar recursos adicionais**. Mantenha a seleção padrão e clique em **Continuar para criar seu recurso**.

3. Na página **Criar Idioma**, configure-o com as seguintes configurações:
    - **Assinatura**: *sua assinatura do Azure*;
    - **Grupo de recursos**: *selecione ou crie um grupo de recursos com um nome exclusivo*;
    - **Região**: *Leste dos EUA*;
    - **Nome**: *Insira um nome exclusivo*;
    - **Nível de preços**: *F0 grátis ou S se F0 grátis não estiver disponível*;
    - **Ao marcar esta caixa, confirmo que li e compreendi todos os termos abaixo**: *Selecionado*;
4. Selecione **Revisar + criar** e depois **Criar** e aguarde a conclusão da implantação.

</details>
<details>
<summary>Configure seu recurso no Azure AI Language Studio</summary>

Em seguida, conecte o recurso de serviços de IA do Azure provisionado acima ao Vision Studio.

1. Em outra guia do navegador, abra o Language Studio em https://language.cognitive.azure.com e entre.

2. Quando solicitado com Select an Azure resource , faça as seguintes configurações:
    - **Diretório do Azure**: *diretório padrão, o diretório que você está usando*;
    - **Assinatura do Azure**: *selecione a assinatura que você está usando*;
    - **Tipo de recurso**: *Idioma*;
    - **Nome do recurso**: *selecione o recurso de serviço de idioma que você acabou de criar*;
3. Em seguida, selecione **Concluído**.

> [!IMPORTANT]
> A partir de julho de 2023, os serviços de IA do Azure abrangem tudo o que era anteriormente conhecido como Serviços Cognitivos e Serviços de IA Aplicados do Azure. Algumas interfaces de usuário ainda estão atualizando suas referências de Cognitive Servicespara Azure AI services. Os dois nomes referem-se ao mesmo tipo de recurso.

> [!OBSERVATION]
> Se você não for solicitado a escolher um recurso de idioma, pode ser porque você possui vários recursos de idioma em sua assinatura; nesse caso:
>   - Na barra na parte superior da página, selecione **Configurações (⚙)**.
>   - Na página **Configurações**, visualize a guia **Recursos**.
>   - Selecione o recurso que você acabou de criar e selecione **Alternar recurso**. Certifique-se de que a identidade gerenciada esteja **habilitada**.

>   - No topo da página, selecione **Language Studio** para retornar à página inicial do Language Studio.

</details>
<details>
<summary>Analise avaliações no Language Studio</summary>
  
1. Num navegador web, navegue até **Language Studio** em https://language.cognitive.azure.com.

2. Na página inicial **Bem-vindo ao Language Studio**, **selecione a guia Classificar texto** e, em seguida, selecione o bloco **Analisar sentimento e extrair opiniões**.

3. Em *Selecionar idioma do texto*, selecione **Inglês**.

4. Em *Selecione seu recurso do Azure*, selecione seu recurso.

5. Em *Digite seu próprio texto, carregue um arquivo ou use um de nossos textos de exemplo*, copie e cole a seguinte revisão:

    "Tired hotel with poor service
     The Royal Hotel, London, United Kingdom
     5/6/2018
     This is an old hotel (has been around since 1950's) and the room furnishings are average - becoming a bit old now and require changing. The internet didn't work and had to come to one of their office rooms to check in for my flight home. The website says it's close to the British Museum, but it's too far to walk."

6. Marque a caixa para confirmar que a demonstração incorrerá em uso e poderá gerar custos e selecione **Executar**.
      - Nos **Detected attributes**, qualquer texto encontrado na imagem é organizado em uma estrutura hierárquica de regiões, linhas e palavras.
      - Na imagem, a localização do texto é indicada por uma caixa delimitadora, conforme mostrado aqui:

7. Revise a saída. Observe que o *documento* é analisado quanto ao sentimento, assim como cada *frase*. Selecione **Frase 1** para mostrar a análise de sentimento dessa frase.

Observe que há um sentimento geral seguido por pontuações próximas a três categorias: *pontuação positiva*, *pontuação neutra* e *pontuação negativa*. Em cada uma das categorias é atribuída uma pontuação entre 0 e 1. Essas pontuações de confiança indicam a probabilidade do texto fornecido ser um sentimento específico.

Selecione a **frase 1** novamente para fechar.

1. Role para cima para selecionar **Limpar caixa de texto** e copie e cole a seguinte revisão:

    "Good Hotel and staff
     The Royal Hotel, London, UK
     3/2/2018
     Clean rooms, good service, great location near Buckingham Palace and Westminster Abbey, and so on. We thoroughly enjoyed our stay. The courtyard is very peaceful and we went to a restaurant which is part of the same group and is Indian ( West coast so plenty of fish) with a Michelin Star. We had the taster menu which was fabulous. The rooms were very well appointed with a kitchen, lounge, bedroom and enormous bathroom. Thoroughly recommended."

2. Selecione **Executar**. Revise o resultado e o sentimento e o nível de confiança.

3. Selecione **Limpar** caixa de texto novamente e copie e cole a seguinte revisão:
    "Very noisy and rooms are tiny The Lombard Hotel, San Francisco, USA 9/5/2018 Hotel is located on Lombard street which is a very busy SIX lane street directly off the Golden Gate Bridge. Traffic from early morning until late at night especially on weekends. Noise would not be so bad if rooms were better insulated but they are not. Had to put cotton balls in my ears to be able to sleep–was too tired to enjoy the city the next day. Rooms are TINY. I picked the room because it had two queen size beds–but the room barely had space to fit them. With family of four in the room it was tight. With all that said, rooms are clean and they’ve made an effort to update them. The hotel is in Marina district with lots of good places to eat, within walking distance to Presidio. May be good hotel for young stay-up-late adults on a budget"

4. Selecione **Executar** e analise o sentimento juntamente com o nível de confiança. Dê uma olhada no texto e compare-o com a análise de sentimento que o serviço retornou.

Neste exercício você usou o Language Studio para criar um novo recurso de idioma ou usar um recurso de idioma existente. Você habilitou o recurso em Configurações antes de experimentar o serviço de mineração de sentimento e opinião. Em seguida, você testou o serviço com três trechos de texto.

</details>
<details>
<summary>Excluir</summary>

Se não pretende fazer mais exercícios, exclua todos os recursos que não precisa mais. Isso evita acumular custos desnecessários.

1. Abra o **portal do Azure** em https://portal.azure.com e selecione o grupo de recursos que contém o recurso que você criou.
2. Selecione o recurso e selecione **Delete** e depois **Yes** para confirmar. O recurso é então excluído.
</details>
