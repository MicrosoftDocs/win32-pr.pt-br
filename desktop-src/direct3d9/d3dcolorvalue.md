---
description: Descreve os valores de cor.
ms.assetid: 6af8c2ec-bc79-4dc6-b56d-7a7676a50b39
title: Estrutura D3DCOLORVALUE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1fe2f187921749207bbbf51d7fcfd75357a70858
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298531"
---
# <a name="d3dcolorvalue-structure-d3d9typesh"></a>Estrutura D3DCOLORVALUE (D3D9Types. h)

Descreve os valores de cor.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
```



## <a name="members"></a>Membros

<dl> <dt>

**r**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor de ponto flutuante que especifica o componente vermelho de uma cor. Esse valor geralmente está no intervalo de 0,0 a 1,0. Um valor de 0,0 indica a ausência completa do componente vermelho, enquanto um valor de 1,0 indica que o vermelho está totalmente presente.

</dd> <dt>

**m**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor de ponto flutuante que especifica o componente verde de uma cor. Esse valor geralmente está no intervalo de 0,0 a 1,0. Um valor de 0,0 indica a ausência completa do componente verde, enquanto um valor de 1,0 indica que o verde está totalmente presente.

</dd> <dt>

**b**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor de ponto flutuante que especifica o componente azul de uma cor. Esse valor geralmente está no intervalo de 0,0 a 1,0. Um valor de 0,0 indica a ausência completa do componente azul, enquanto um valor de 1,0 indica que o azul está totalmente presente.

</dd> <dt>

**um**
</dt> <dd>

Tipo: **float**

</dd> <dd>

Valor de ponto flutuante que especifica o componente alfa de uma cor. Esse valor geralmente está no intervalo de 0,0 a 1,0. Um valor de 0,0 indica totalmente transparente, enquanto um valor de 1,0 indica totalmente opaco.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode definir os membros dessa estrutura com valores fora do intervalo de 0 a 1 para implementar alguns efeitos incomuns. Valores maiores que 1 produzem luzes fortes que tendem a desbotar uma cena. Valores negativos produzem luzes escuras que realmente removem a luz de uma cena.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas do Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 




