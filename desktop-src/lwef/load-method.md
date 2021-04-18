---
title: Método Load
description: Método Load
ms.assetid: 72a37471-f69b-49a5-a6eb-d65bff970c0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0927fc8e49e55c2bdfcd7b1109bb8604540c199c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105784535"
---
# <a name="load-method"></a>Método Load

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Carrega um caractere na coleção de [**caracteres**](/windows/desktop/lwef/the-characters-object) .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

*agente do ***. Caracteres. Load "*** characterid * * *",* *  *provedor*



| Parte          | Descrição                                                                                                                                                                                                                              |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Caractere de caracteres* | Obrigatórios. Um valor de cadeia de caracteres que será usado para se referir aos dados de caractere a serem carregados.                                                                                                                                                  |
| *Provedor*    | Obrigatórios. Um tipo de dados Variant que deve ser um dos seguintes: **filespec** o local do arquivo local do arquivo de definição do caractere especificado. <br/> **URL** do O endereço HTTP para o arquivo de definição do caractere.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode carregar caracteres do subdiretório do agente especificando um caminho relativo (um que não inclui dois pontos ou um caractere de barra à esquerda). Isso prefixa o caminho com o diretório de caracteres do agente (localizado no diretório localizado do Windows \\ MSAgent). Por exemplo, especificar o seguinte carregaria gênio. ACS do diretório de caracteres do agente:


```
   Agent.Character.Load "genie", "genie.acs"
```



Você também pode especificar seu próprio diretório no diretório de caracteres do agente.


```
   Agent.Character.Load "genie", "MyCharacters\genie.acs"
```



Você pode carregar o caractere definido atualmente como o caractere padrão do usuário atual, não incluindo um caminho como o segundo parâmetro do método **Load** .


```
   Agent.Character.Load "character"
```



Não é possível carregar o mesmo caractere (um caractere com o mesmo GUID) mais de uma vez a partir de uma única instância do controle. Da mesma forma, você não pode carregar o caractere padrão e outros caracteres ao mesmo tempo de uma única instância do controle porque o caractere padrão pode ser o mesmo que o outro caractere. Se você tentar fazer isso, o servidor gerará um erro. No entanto, você pode criar outra instância do controle Agent e carregar o mesmo caractere.

O Provedor de Dados do Microsoft Agent dá suporte ao carregamento de dados de caracteres armazenados como um único arquivo estruturado (. ACS) com dados de caractere e dados de animação juntos ou como dados de caractere separados (. ACF) e animação (. ACA) arquivos. Use estrutura única. Arquivo ACS para carregar um caractere que é armazenado em um disco ou rede local e acessado usando um protocolo de arquivo convencional (como caminhos UNC). Use a separada. ACF e. ACA arquivos quando você deseja carregar os arquivos de animação individualmente de um site remoto onde eles são acessados usando o protocolo HTTP.

Fins. Os arquivos ACS, usando o método **Load** , fornecem acesso às animações de um caractere. Fins. Arquivos ACF, você também usa o método [**Get**](get-method.md) para carregar dados de animação. O método **Load** não oferece suporte ao download. Arquivos ACS de um site HTTP.

O carregamento de um caractere não exibe automaticamente o caractere. Use o método [**show**](show-method.md) primeiro para tornar o caractere visível.

Se você usar o método **Load** para carregar um arquivo de caracteres armazenado no computador local e a chamada falhar; por exemplo, como o arquivo não foi encontrado, o Agent gera um erro. Você pode usar o suporte em sua linguagem de programação para fornecer uma rotina de tratamento de erros para detectar e processar o erro.


```
   Sub Form_Load
      On Error GoTo ErrorHandler
      Agent1.Characters.Load "mychar", "genie.acs"
      ' Successful load
      . . .
      Exit Sub
      ErrorHandler:
      ' Unsuccessful load
      . . .
      Resume Next
   End Sub
```



Você também pode manipular o erro definindo [**RaiseRequestErrors**](https://www.bing.com/search?q=**RaiseRequestErrors**) como **false**, declarando um objeto e atribuindo a solicitação de **carregamento** a ele. Em seguida, siga a chamada de **carregamento** com uma instrução que verifica o status do objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .


```
Dim LoadRequest as Object

   Sub Form_Load
      Agent1.RaiseRequestErrors = False
      Set LoadRequest = Agent1.Characters.Load _
         ("mychar", "c:\some directory\some character.acs")
      If LoadRequest.Status Not 0 Then
         ' Unsuccessful load
         . . .
         Exit Sub
      Else 
         ' Successful load
         . . .
   End Sub
```



Se você carregar um caractere que não seja local; por exemplo, usando o protocolo HTTP, você também pode verificar se há uma falha de **carregamento** atribuindo um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) ao método **Load** . No entanto, como esse método de carregamento de um caractere é manipulado de forma assíncrona, verifique seu status no evento [**RequestComplete**](requestcomplete-event.md) . Essa técnica não funcionará para carregar um caractere usando o protocolo UNC, pois o método **Load** é processado de forma síncrona.

 

