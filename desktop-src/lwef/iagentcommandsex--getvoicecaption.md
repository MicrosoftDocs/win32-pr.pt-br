---
title: IAgentCommandsEx GetVoiceCaption
description: IAgentCommandsEx GetVoiceCaption
ms.assetid: 0e505295-386a-421f-a43c-6da03c8a2b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec2a6d5138b9b7074d1c9a2002f45a0076fe5d957ae5e47d865c693f73e8b37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609426"
---
# <a name="iagentcommandsexgetvoicecaption"></a>IAgentCommandsEx::GetVoiceCaption

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption
);
```

Recupera o [**VoiceCaption para**](voicecaption-property.md) um [**objeto Command.**](/windows/desktop/lwef/the-command-object)

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*
</dt> <dd>

O endereço de um BSTR que recebe o valor do texto [**Legenda**](caption-property.md) exibido para um [**Comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

O texto retornado é definido para o objeto [**Command**](/windows/desktop/lwef/the-command-object) e aparece na janela Comandos de Voz quando o aplicativo cliente está ativo de entrada.

Essa propriedade se aplica somente ao uso do caractere pelo aplicativo cliente; A configuração não afeta outros clientes do caractere ou outros caracteres do aplicativo cliente.

## <a name="see-also"></a>Consulte Também

[**IAgentCommandsEx::SetVoiceCaption**](iagentcommandsex--setvoicecaption.md)


 

 