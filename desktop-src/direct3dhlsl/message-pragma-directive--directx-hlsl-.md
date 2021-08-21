---
title: Diretiva de pragma da mensagem
description: A diretiva pragma que produz mensagens de tempo de compilador.
ms.assetid: dc3ece10-9730-4ab1-acc8-f95abc92de7d
keywords:
- HLSL de diretiva de pragma de mensagem
topic_type:
- apiref
api_name:
- message pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fce4b8f2fec887397794914604a0755049615699af77c5572536b5758bda2d88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986356"
---
# <a name="message-pragma-directive"></a>Diretiva de pragma da mensagem

A diretiva pragma que produz mensagens de tempo de compilador.



| \#mensagem pragma ("*token-String*") |
|-----------------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                                                    | Descrição                  |
|-----------------------------------------------------------------------------------------|------------------------------|
| <span id="token-string"></span><span id="TOKEN-STRING"></span>*Cadeia de caracteres de token*<br/> | Mensagem do compilador.<br/> |



 

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra o processamento de mensagens durante o pré-processamento.


```
#pragma message "Debugging flag set."
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Diretivas de pré-processador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Diretiva pragma (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





