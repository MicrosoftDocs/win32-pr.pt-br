---
title: IAgentCharacterEx GetSRModeID
description: IAgentCharacterEx GetSRModeID
ms.assetid: 28049680-8245-49f3-9ecd-13c7605f10ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0bba237fb1bc1b5d769f7e8ecf983b58718c18e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "103640224"
---
# <a name="iagentcharacterexgetsrmodeid"></a>IAgentCharacterEx::GetSRModeID

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetSRModeID(
   BSTR * pbszModeID  // address of speech recognition engine ID
);
```

Recupera a ID de modo do mecanismo de reconhecimento de fala definido para o caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*
</dt> <dd>

Endereço de um BSTR que recebe a configuração de ID de modo do mecanismo de reconhecimento de fala para o caractere.

</dd> </dl>

Essa configuração retorna o mecanismo definido para a entrada de fala de um caractere. A ID de modo para um mecanismo de reconhecimento de fala é uma representação de cadeia de caracteres do GUID (formatado com chaves e traços) pelo fornecedor de fala identificando exclusivamente o mecanismo. Para obter mais informações, consulte a [documentação do SDK do Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).

Se você não definir uma ID de modo de mecanismo de reconhecimento de fala para o caractere, o servidor retornará um mecanismo que corresponda à configuração de idioma do caractere (usando as interfaces do Microsoft Speech API). Se não houver nenhum mecanismo de reconhecimento de fala correspondente disponível para o caractere, o servidor retornará uma cadeia de caracteres nula (vazia).

Quando a entrada de fala está habilitada (na janela Opções de caractere avançado), a consulta ou a configuração dessa propriedade carregará o mecanismo associado (se ele ainda não estiver carregado) e iniciará os serviços de fala. Ou seja, a chave de escuta está disponível e a dica de escuta é exibível. (A chave de escuta e a dica de escuta serão habilitadas somente se elas também estiverem habilitadas em opções de caractere avançadas.) No entanto, se você consultar a propriedade quando a fala estiver desabilitada, o servidor não iniciará os serviços de fala e retornará uma cadeia de caracteres nula (cadeia de caracteres vazia).

Essa função retorna apenas a configuração para o uso do caractere do aplicativo cliente; a configuração não reflete outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

Essa função não falhará se [**IAgentSpeechInputProperties:: Getabilited**](iagentspeechinputproperties--getenabled.md) retornar **false**.

Os requisitos do mecanismo de fala do Microsoft Agent são baseados no Microsoft Speech API. Os mecanismos que dão suporte aos requisitos SAPI do Microsoft Agent podem ser instalados e usados com o Agent.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacterEx::SetSRModeID**](iagentcharacterex--setsrmodeid.md)


 

 




