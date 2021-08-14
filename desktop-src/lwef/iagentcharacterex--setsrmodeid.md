---
title: IAgentCharacterEx SetSRModeID
description: IAgentCharacterEx SetSRModeID
ms.assetid: 8f9072ec-1f64-4f5c-972d-cd6799ce028c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7fcfbf4aff25c1af0fbdb1f40471f6b54c4731f22fb2c736da42fe462eb390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750413"
---
# <a name="iagentcharacterexsetsrmodeid"></a>IAgentCharacterEx::SetSRModeID

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetSRModeID(
   BSTR bszModeID  // speech recognition engine ID
);
```

Define a ID do modo do mecanismo de reconhecimento de fala definido para o caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

bszModeID

A configuração de ID de modo do mecanismo de reconhecimento de fala para o caractere.

Essa configuração define o mecanismo para a entrada de fala de um caractere. A ID do modo para um mecanismo de reconhecimento de fala é o GUID definido pelo fornecedor de fala que identifica exclusivamente o modo do mecanismo (formatado com chaves e traços). Para obter mais informações, consulte a [documentação do SDK de Fala da Microsoft](https://msdn.microsoft.com/library/ee705648.aspx).

Se você especificar uma ID de modo que não corresponder à configuração de idioma do caractere, se o usuário tiver desabilitado o reconhecimento de fala (na folha de propriedades do Microsoft Agent) ou se o mecanismo não estiver instalado, essa chamada falhará. Se você não definir uma ID de modo de mecanismo de reconhecimento de fala para o caractere, o servidor definirá uma que corresponde à configuração de idioma do caractere (usando interfaces Speech API Microsoft).

Quando a entrada de fala estiver habilitada na folha de propriedades do Agent (Opções de Caractere Avançadas), definir essa propriedade carregará o mecanismo associado (se ainda não estiver carregado) e iniciará os serviços de fala. Ou seja, a tecla Listening está disponível e a Dica de Escuta é exibida. (A tecla Escuta e a Dica de Escuta só serão habilitadas se também estão habilitadas em Opções Avançadas de Caracteres.) No entanto, se você consultar a propriedade quando a fala estiver desabilitada, o servidor não iniciará os serviços de fala.

Essa propriedade se aplica somente ao cliente do caractere; a configuração não reflete a configuração para outros clientes do caractere ou outros caracteres do cliente.

Os requisitos do mecanismo de fala do Microsoft Agent são baseados no Microsoft Speech API. Os mecanismos que suportam os requisitos de SAPI do Microsoft Agent podem ser instalados e usados com o Agent.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md)


 

 




