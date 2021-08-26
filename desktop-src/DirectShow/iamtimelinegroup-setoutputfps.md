---
description: O método SetOutputFPS define a taxa de quadros de saída descompactada para esse grupo.
ms.assetid: 335ea106-d5db-43a1-b771-b027e25164a6
title: Método IAMTimelineGroup::SetOutputFPS (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 332e9ea33e0ca559800e560409066946247d1cff34b8e6b48fd1fadbdb91e38f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052696"
---
# <a name="iamtimelinegroupsetoutputfps-method"></a>Método IAMTimelineGroup::SetOutputFPS

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SetOutputFPS` método define a taxa de quadros de saída descompactada para esse grupo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetOutputFPS(
   double FPS
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Fps* 
</dt> <dd>

Taxa de quadros de saída para esse grupo, em quadros por segundo. O valor não pode ser igual a zero e não pode ter mais de sete dígitos após a casa decimal.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

A saída renderizada desse grupo é executado na taxa de quadros especificada e todas as edições no material de origem são arredondadas para o limite de quadro mais próximo, conforme definido pela taxa de quadros. Para melhor desempenho, use a mesma taxa de quadros para todos os grupos, vídeo e áudio.

O [**método IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) substitui a taxa de quadros.

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAMTimelineGroup Interface**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




