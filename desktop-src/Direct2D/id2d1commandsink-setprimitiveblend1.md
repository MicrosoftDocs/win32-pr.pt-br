---
title: Método ID2D1CommandSink1 SetPrimitiveBlend1
description: Define um novo modo de mesclagem primitiva.
ms.assetid: 3EA9EC07-1B2F-48A2-ABFB-2DA0E2EFFBF4
keywords:
- Método SetPrimitiveBlend1 Direct2D
- Método SetPrimitiveBlend1 Direct2D, interface ID2D1CommandSink1
- ID2D1CommandSink1 interface Direct2D, método SetPrimitiveBlend1
topic_type:
- apiref
api_name:
- ID2D1CommandSink1.SetPrimitiveBlend1
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3aa961eec873cc84e5b34ce41279c09f580e63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085496"
---
# <a name="id2d1commandsink1setprimitiveblend1-method"></a>Método ID2D1CommandSink1:: SetPrimitiveBlend1

Define um novo modo de mesclagem primitiva.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetPrimitiveBlend1(
   D2D1_PRIMITIVE_BLEND primitiveBlend
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*primitiveBlend* 
</dt> <dd>

Tipo: **[ **d2d1 \_ PRIMITIVE \_ Blend**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**

A mistura primitiva que será aplicada aos primitivos subsequentes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se o método for bem sucedido, ele retornará **S \_ OK**. Se falhar, ele retornará um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

### <a name="blend-modes"></a>Modos do Blend

Para a renderização com alias (exceto para o modo MIN), o valor de saída O é calculado por meio da interpolação linear do valor *Blend (S, D)* com o valor de pixel de destino, com base no valor que o primitivo cobre o pixel de destino.

A tabela aqui mostra os modos de mistura primitivos para mesclagem com alias e suavização de alias. As equações listadas na tabela usam estes elementos:

-   O = saída
-   S = origem
-   SA = origem alfa
-   D = destino
-   DA = destino alfa
-   C = cobertura de pixel



| Modo de mesclagem primitiva                 | Mesclagem com alias                            | Mesclagem AntiAlias            | Descrição                                                                                                              |
|--------------------------------------|---------------------------------------------|---------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| \_Origem de \_ mesclagem primitiva \_ de d2d1 \_ | O = (S + (1 SA) \* D) \* C + D \* (1 C) | O = S \* C + D \* (1 SA \* c)   | O modo de mesclagem de origem por destino padrão.                                                                         |
| \_Cópia de \_ mistura \_ primitiva de d2d1         | O = S \* C + D \* (1 C)                   | O = S \* C + D \* (1 C)       | A origem é copiada para o destino; os pixels de destino são ignorados.                                             |
| D2D1 \_ PRIMITIVE \_ Blend \_ min          | O = min (S + 1-SA, D)                        | O = min (S \* c + 1 SA \* c, D) | Os valores de pixel resultantes usam o mínimo dos valores de pixel de origem e de destino. Disponível no Windows 8 e posterior. |
| \_Adição de \_ mistura \_ primitiva de d2d1          | O = (S + D) \* C + D \* (1 C)             | O = S \* C + D                  | Os valores de pixel resultantes são a soma dos valores de pixel de origem e de destino. Disponível no Windows 8 e posterior.     |



 

![uma ilustração dos modos de mesclagem primitiva de Direct2D com opacidade e planos de fundo variados.](images/primblenddemo.png)

Uma ilustração dos modos de mistura primitiva com opacidade e planos de fundo variados.

O primitivo Blend será aplicado a todos os primitivos desenhados no contexto, a menos que isso seja substituído pelo parâmetro *compositemode* na API do [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) .

O primitivo Blend se aplica ao interior de quaisquer primitivos desenhados no contexto. No caso do [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)), isso será implícito pelo retângulo da imagem, pelo deslocamento e pela transformação do mundo.

Se o primitivo Blend for algo diferente de **d2d1 \_ primitiva \_ Blend \_** , a renderização de ClearType será desativada. Se o aplicativo forçar explicitamente a renderização de ClearType nesses modos, o contexto de desenho será colocado em um estado de erro. \_ \_ O estado incorreto do D2DERR será retornado de [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                          |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID2D1CommandSink1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1commandsink1)
</dt> </dl>

 

