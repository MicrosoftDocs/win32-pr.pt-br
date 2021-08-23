---
title: IAgentCharacterEx GetTTSModeID
description: IAgentCharacterEx GetTTSModeID
ms.assetid: e7b3c576-dc3c-40de-8d09-8e7f4b79250b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3e6bc029a6fce1da3d6f920a25ccc86c49619751a6bd43f865154bd7a235696
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105484"
---
# <a name="iagentcharacterexgetttsmodeid"></a>IAgentCharacterEx::GetTTSModeID

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetTTSModeID(
   BSTR * pbszModeID  // address of TTS engine ID
);
```

Recupera a ID do modo do mecanismo TTS definido para o caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*
</dt> <dd>

Endereço de um BSTR que recebe a configuração de ID de modo do mecanismo TTS para o caractere.

</dd> </dl>

Essa configuração retorna a ID do modo de mecanismo TTS (texto em fala) para a saída falada de um caractere. A ID do modo para um mecanismo TTS é uma representação de cadeia de caracteres do GUID (formatada com chaves e traços) definida pelo fornecedor de fala identificando exclusivamente o mecanismo. Para obter mais informações, consulte a [documentação do SDK de Fala da Microsoft](https://msdn.microsoft.com/library/ee705648.aspx). Consultar essa propriedade carregará o mecanismo associado se ele ainda não estiver carregado.

Se você não definir uma ID de modo de mecanismo TTS para o caractere, o servidor tentará retornar um mecanismo que corresponde (usando interfaces do Microsoft Speech API) a configuração TTS compilada do caractere e a configuração de idioma atual do caractere. Se eles são diferentes, a configuração de idioma do caractere substitui sua configuração de modo autor. Se você não tiver definido a configuração de idioma do caractere, o idioma do caractere será a ID de idioma padrão do usuário e o servidor tentará a corresponder com base nessa ID de idioma.

Essa função não falhará se [**IAgentAudioObjectProperties::GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) retornar **False.**

Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.

Os requisitos do mecanismo de fala do Microsoft Agent são baseados no Microsoft Speech API. Os mecanismos que suportam os requisitos de SAPI do Microsoft Agent podem ser instalados e usados com o Agent.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacterEx::SetTTSModeID**](iagentcharacterex--setttsmodeid.md)


 

 




