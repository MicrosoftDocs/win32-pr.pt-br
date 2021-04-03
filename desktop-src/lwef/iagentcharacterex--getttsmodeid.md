---
title: IAgentCharacterEx GetTTSModeID
description: IAgentCharacterEx GetTTSModeID
ms.assetid: e7b3c576-dc3c-40de-8d09-8e7f4b79250b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a77e78755345c0993ed5723080b0b3f4b8297a
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104007189"
---
# <a name="iagentcharacterexgetttsmodeid"></a>IAgentCharacterEx::GetTTSModeID

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetTTSModeID(
   BSTR * pbszModeID  // address of TTS engine ID
);
```

Recupera a ID de modo do mecanismo TTS definido para o caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*
</dt> <dd>

Endereço de um BSTR que recebe a configuração de ID de modo do mecanismo de TTS para o caractere.

</dd> </dl>

Essa configuração retorna a ID do modo de mecanismo de TTS (conversão de texto em fala) para a saída falada de um caractere. A ID de modo para um mecanismo de TTS é uma representação de cadeia de caracteres do GUID (formatado com chaves e traços) definido pelo fornecedor de fala identificando exclusivamente o mecanismo. Para obter mais informações, consulte a [documentação do SDK do Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx). A consulta dessa propriedade carregará o mecanismo associado se ele ainda não estiver carregado.

Se você não definir uma ID de modo de mecanismo TTS para o caractere, o servidor tentará retornar um mecanismo que corresponda (usando as interfaces do Microsoft Speech API) a configuração de TTS compilada do caractere e a configuração de idioma atual do caractere. Se forem diferentes, a configuração de idioma do caractere substituirá sua configuração de modo criado. Se você não tiver definido a configuração de idioma do caractere, o idioma do caractere será a ID de idioma padrão do usuário e o servidor tentará a correspondência com base na ID do idioma.

Essa função não falhará se [**IAgentAudioObjectProperties:: Getabilited**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) retornar **false**.

Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

Os requisitos do mecanismo de fala do Microsoft Agent são baseados no Microsoft Speech API. Os mecanismos que dão suporte aos requisitos SAPI do Microsoft Agent podem ser instalados e usados com o Agent.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacterEx::SetTTSModeID**](iagentcharacterex--setttsmodeid.md)


 

 




