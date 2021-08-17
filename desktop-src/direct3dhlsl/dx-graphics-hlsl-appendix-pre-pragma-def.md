---
title: Diretiva pragma def
description: Diretiva pragma que aloca manualmente um registro de sombreador de ponto flutuante.
ms.assetid: 45db94c4-f6f6-4c88-9bf2-4eaa9abf7844
keywords:
- Diretiva pragma def HLSL
topic_type:
- apiref
api_name:
- def pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe6961f5fd8c05f291af3634c07de6befada0efa54586796ca881bffe893bf5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726436"
---
# <a name="def-pragma-directive"></a>Diretiva pragma def

Diretiva pragma que aloca manualmente um registro de sombreador de ponto flutuante.



| \#pragma def ( *destino*, *registro*, *val1*, *val2*,*Val3*, *val4* ) |
|---------------------------------------------------------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                                        | Descrição                                                                 |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="target"></span><span id="TARGET"></span>*alvo*<br/>       | Destino que contém o registro a ser alocado. <br/>                  |
| <span id="register"></span><span id="REGISTER"></span>*Registr*<br/> | Registro de sombreador de ponto flutuante para alocar. <br/>                     |
| <span id="val0"></span><span id="VAL0"></span>*val0*<br/>             | Primeiro byte do valor a ser alocado para o registro especificado. <br/>  |
| <span id="val1"></span><span id="VAL1"></span>*val1*<br/>             | Segundo byte do valor a ser alocado para o registro especificado. <br/> |
| <span id="val2"></span><span id="VAL2"></span>*val2*<br/>             | Terceiro byte do valor a ser alocado para o registro especificado. <br/>  |
| <span id="val3"></span><span id="VAL3"></span>*val3*<br/>             | Quarto byte do valor a ser alocado para o registro especificado. <br/> |



 

## <a name="remarks"></a>Comentários

O pragma def permite que um desenvolvedor preencha um registro de sombreador de ponto flutuante com o valor especificado. Esse pragma é usado raramente.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Diretivas de pré-processador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Diretiva pragma (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





