---
title: IAgentCharacterEx SetTTSModeID
description: IAgentCharacterEx SetTTSModeID
ms.assetid: 66ed792a-1693-45dc-b9a8-eebe772c5af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34392e65fcb8f3a46db6251f01f59ad76aba278d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365671"
---
# <a name="iagentcharacterexsetttsmodeid"></a>IAgentCharacterEx::SetTTSModeID

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetTTSModeID(
   BSTR bszModeID  // TTS engine ID
);
```

Define a ID de modo do mecanismo de TTS definido para o caractere.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszModeID*
</dt> <dd>

A configuração de ID de modo do mecanismo de TTS para o caractere.

> [!Note]  
> **IAgentCharacterEx: SetTTSModeID** pode falhar se o Speech.dll não estiver instalado e o mecanismo especificado não corresponder à configuração do modo TTS compilado do caractere.

 

</dd> </dl>

Essa configuração determina o modo de mecanismo preferencial para a saída de TTS falada de um caractere. A ID de modo para um mecanismo de TTS (conversão de texto em fala) é o GUID definido pelo fornecedor de fala que identifica exclusivamente o modo do mecanismo (formatado com chaves e traços). Para obter mais informações, consulte a [documentação do SDK do Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).

Se você definir uma ID de modo TTS, ela substituirá a tentativa do servidor de corresponder a um mecanismo de fala com base na ID do modo TTS compilado do caractere, na ID do idioma atual do sistema e na ID de idioma atual do caractere. No entanto, se você tentar definir uma ID de modo quando o usuário tiver desabilitado a saída de fala na folha de propriedades do Microsoft Agent ou quando o mecanismo associado não estiver instalado, essa chamada falhará.

Se você não definir uma ID de modo de mecanismo TTS para o caractere, o servidor definirá um mecanismo que corresponda à configuração de idioma do caractere (usando as interfaces do Microsoft Speech API). A definição dessa propriedade carregará o mecanismo associado se ele ainda não estiver carregado.

Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.

Os requisitos do mecanismo de fala do Microsoft Agent são baseados no Microsoft Speech API. Os mecanismos que dão suporte aos requisitos SAPI do Microsoft Agent podem ser instalados e usados com o Agent.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacterEx:GetTTSModeID**](iagentcharacterex--getttsmodeid.md)


 

 




