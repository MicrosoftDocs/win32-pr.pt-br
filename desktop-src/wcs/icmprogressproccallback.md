---
title: Função de retorno de chamada ICMProgressProcCallback
description: A função ICMProgressProcCallback é uma função de retorno de chamada fornecida pelo aplicativo que relata o progresso e permite que o aplicativo cancele o processamento de cores.
ms.assetid: 4e0bfa4c-f0eb-4776-98d6-90d9adf71bee
keywords:
- Função de retorno de chamada ICMProgressProcCallback sistema de cores do Windows
topic_type:
- apiref
api_name:
- ICMProgressProcCallback
api_location:
- Icm.h
api_type:
- UserDefined
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8acf790a135a41e4eabb4a67c2498f1ed914c4c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769668"
---
# <a name="icmprogressproccallback-callback-function"></a>Função de retorno de chamada ICMProgressProcCallback

A função **ICMProgressProcCallback** é uma função de retorno de chamada fornecida pelo aplicativo que relata o progresso e permite que o aplicativo cancele o processamento de cores.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI ICMProgressProcCallback(
   ULONG  ulMax,
   ULONG  ulCurrent,
   LPARAM ulCallbackData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ulMax* 
</dt> <dd>

Especifica o valor máximo do contador de progresso (usado para estimar a conclusão do processamento de bitmap).

</dd> <dt>

*ulCurrent* 
</dt> <dd>

Especifica o valor atual do contador de progresso (quando dividido pelo valor máximo, fornece uma estimativa aproximada da porcentagem de conclusão).

</dd> <dt>

*ulCallbackData* 
</dt> <dd>

Especifica os dados que são passados pelo aplicativo para uma função ICM2, que então o passa para a função de retorno de chamada. Esses dados podem ser usados, por exemplo, para identificar o bitmap e o processo sobre o qual o progresso está sendo relatado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função retorna **true** para continuar o processamento de bitmap. O valor de retorno é **false** para cancelar o processamento. Se o processamento for cancelado, a função de chamada retornará zero para indicar falha, embora seu buffer de saída possa ser parcialmente preenchido.

## <a name="remarks"></a>Comentários

O nome dessa função de retorno de chamada é fornecido pelo aplicativo. Várias funções WCS, incluindo [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) e [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits), chamam essa função periodicamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>ICM. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Conceitos básicos de gerenciamento de cores](basic-color-management-concepts.md)
</dt> <dt>

[Funções](functions.md)
</dt> <dt>

[**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits)
</dt> <dt>

[**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits)
</dt> </dl>
