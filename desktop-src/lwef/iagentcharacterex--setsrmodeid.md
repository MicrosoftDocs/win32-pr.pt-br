---
title: IAgentCharacterEx SetSRModeID
description: IAgentCharacterEx SetSRModeID
ms.assetid: 8f9072ec-1f64-4f5c-972d-cd6799ce028c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390d7e0126fe5ef62273cf6d7d23ada25c26bbdb
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104453850"
---
# <a name="iagentcharacterexsetsrmodeid"></a>IAgentCharacterEx::SetSRModeID

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetSRModeID(
   BSTR bszModeID  // speech recognition engine ID
);
```

Define a ID de modo do mecanismo de reconhecimento de fala definido para o caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

bszModeID

A configuração de ID de modo do mecanismo de reconhecimento de fala para o caractere.

Essa configuração define o mecanismo para a entrada de fala de um caractere. A ID de modo para um mecanismo de reconhecimento de fala é o GUID definido pelo fornecedor de fala que identifica exclusivamente o modo do mecanismo (formatado com chaves e traços). Para obter mais informações, consulte a [documentação do SDK do Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).

Se você especificar uma ID de modo que não corresponda à configuração de idioma do caractere, se o usuário tiver desabilitado o reconhecimento de fala (na folha de propriedades do Microsoft Agent) ou se o mecanismo não estiver instalado, essa chamada falhará. Se você não definir uma ID de modo de mecanismo de reconhecimento de fala para o caractere, o servidor definirá uma que corresponda à configuração de idioma do caractere (usando as interfaces do Microsoft Speech API).

Quando a entrada de fala está habilitada na folha de propriedades do agente (opções avançadas de caractere), a definição dessa propriedade carregará o mecanismo associado (se ele ainda não estiver carregado) e iniciará os serviços de fala. Ou seja, a chave de escuta está disponível e a dica de escuta é exibível. (A chave de escuta e a dica de escuta serão habilitadas somente se elas também estiverem habilitadas em opções de caractere avançadas.) No entanto, se você consultar a propriedade quando a fala estiver desabilitada, o servidor não iniciará os serviços de fala.

Essa propriedade aplica-se somente ao cliente do caractere; a configuração não reflete a configuração para outros clientes do caractere ou outros caracteres do cliente.

Os requisitos do mecanismo de fala do Microsoft Agent são baseados no Microsoft Speech API. Os mecanismos que dão suporte aos requisitos SAPI do Microsoft Agent podem ser instalados e usados com o Agent.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md)


 

 




