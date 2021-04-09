---
description: Cria uma superfície compactada para a decodificação de aceleração de vídeo do DirectX (DXVA).
ms.assetid: 2bb8c99d-1151-4f6d-869f-2c1a592e76af
title: 'Método IDirect3DVideoDevice9:: CreateSurface (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateSurface
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d9e87c9767619241fd6228bb6b0a531249dd2d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091460"
---
# <a name="idirect3dvideodevice9createsurface-method"></a>Método IDirect3DVideoDevice9:: CreateSurface

Cria uma superfície compactada para a decodificação de aceleração de vídeo do DirectX (DXVA).

Para obter os requisitos de superfície, chame [**IDirect3DVideoDevice9:: GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) e examine as estruturas [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) retornadas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateSurface(
   UINT              Width,
   UINT              Height,
   UINT              BackBuffers,
   D3DFORMAT         Format,
   D3DPOOL           Pool,
   DWORD             Usage,
   IDirect3DSurface9 **ppSurface,
   HANDLE            *pSharedHandle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Largura* 
</dt> <dd>

A largura da superfície, em pixels. Defina esse parâmetro como igual a **DXVACompBufferInfo. WidthToCreate**.

</dd> <dt>

*Altura* 
</dt> <dd>

A altura da superfície, em pixels. Defina esse parâmetro como igual a **DXVACompBufferInfo. HeightToCreate**.

</dd> <dt>

*Backbuffers* 
</dt> <dd>

O número de buffers de fundo. Esse parâmetro pode ser zero.

</dd> <dt>

*Formato* 
</dt> <dd>

O formato de pixel, especificado como um valor **D3DFORMAT** . Defina esse parâmetro como igual a **DXVACompBufferInfo. Format**.

</dd> <dt>

*Pool* 
</dt> <dd>

O pool de memória no qual criar a superfície, especificada como um valor **D3DPOOL** . Defina esse parâmetro como igual a **DXVACompBufferInfo. pool**.

</dd> <dt>

*Usage* 
</dt> <dd>

Uma ou **uma** ou mais constantes de **D3DUSAGE** . Defina esse parâmetro como igual a **DXVACompBufferInfo. Usage**.

</dd> <dt>

*ppSurface* 
</dt> <dd>

Recebe um ponteiro para a interface **IDirect3DSurface9** . O chamador deve liberar a interface.

</dd> <dt>

*pSharedHandle* 
</dt> <dd>

Reservado. Defina como **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




