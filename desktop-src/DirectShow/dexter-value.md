---
description: Identifica uma propriedade que deve ser definida em uma transição ou efeito, juntamente com o número de valores distintos que a propriedade assume sobre a duração da transição ou do efeito.
ms.assetid: 3b1c35cf-f1f7-4f2c-8d94-1aaae4116833
title: Estrutura de DEXTER_VALUE (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_VALUE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 930b828e1b715cfcb53275192ed76a7df7d116ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768603"
---
# <a name="dexter_value-structure"></a>\_Estrutura de valor Dexter

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

Identifica uma propriedade que deve ser definida em uma transição ou efeito, juntamente com o número de valores distintos que a propriedade assume sobre a duração da transição ou do efeito.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  VARIANT        v;
  REFERENCE_TIME rt;
  DWORD          dwInterp;
} DEXTER_VALUE;
```



## <a name="members"></a>Membros

<dl> <dt>

**l**
</dt> <dd>

Valor da propriedade.

</dd> <dt>

**RT**
</dt> <dd>

Hora em que a propriedade assume o valor, em relação ao início da transição ou efeito.

</dd> <dt>

**dwInterp**
</dt> <dd>

Sinalizador que indica como a propriedade progride do valor anterior para esse valor. Deve ser uma destas opções:



| Valor                                                                                                                                                                           | Significado                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="DEXTERF_JUMP"></span><span id="dexterf_jump"></span><dl> <dt>**DEXTERF \_**</dt> </dl>                      | A propriedade salta instantaneamente para o novo valor na hora especificada.<br/>     |
| <span id="DEXTERF_INTERPOLATE"></span><span id="dexterf_interpolate"></span><dl> <dt>**\_interpolação de DEXTERF**</dt> </dl> | A propriedade é interpolada linearmente ao longo do tempo do valor anterior.<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>QEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[**\_parâmetro Dexter**](dexter-param.md)
</dt> </dl>

 

 




