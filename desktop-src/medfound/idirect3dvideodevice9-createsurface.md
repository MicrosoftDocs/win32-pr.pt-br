---
description: Cria uma superfície compactada para decodificação de DXVA (Aceleração de Vídeo) do DirectX.
ms.assetid: 2bb8c99d-1151-4f6d-869f-2c1a592e76af
title: Método IDirect3DVideoDevice9::CreateSurface (Dxva.h)
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
ms.openlocfilehash: b5bc624527c7ef3ea2a8bb9c878f1d97e865a54341ae5902449fb8a015374f3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887866"
---
# <a name="idirect3dvideodevice9createsurface-method"></a>Método IDirect3DVideoDevice9::CreateSurface

Cria uma superfície compactada para decodificação de DXVA (Aceleração de Vídeo) do DirectX.

Para obter os requisitos de superfície, chame [**IDirect3DVideoDevice9::GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) e examine as estruturas [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) retornadas.

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

A largura da superfície, em pixels. De definir esse parâmetro igual **a DXVACompBufferInfo.WidthToCreate**.

</dd> <dt>

*Altura* 
</dt> <dd>

A altura da superfície, em pixels. De definir esse parâmetro igual **a DXVACompBufferInfo.HeightToCreate**.

</dd> <dt>

*BackBuffers* 
</dt> <dd>

O número de buffers de fundo. Esse parâmetro pode ser zero.

</dd> <dt>

*Formato* 
</dt> <dd>

O formato de pixel, especificado como um **valor D3DFORMAT.** De definir esse parâmetro igual **a DXVACompBufferInfo.Format.**

</dd> <dt>

*Pool* 
</dt> <dd>

O pool de memória no qual criar a superfície, especificado como um **valor D3DPOOL.** De definir esse parâmetro igual a **DXVACompBufferInfo.Pool.**

</dd> <dt>

*Usage* 
</dt> <dd>

Um OR bit a **bit** de uma ou mais **constantes D3DUSAGE.** De definir esse parâmetro igual a **DXVACompBufferInfo.Usage.**

</dd> <dt>

*ppSurface* 
</dt> <dd>

Recebe um ponteiro para a interface **IDirect3DSurface9.** O chamador deve liberar a interface.

</dd> <dt>

*pSharedHandle* 
</dt> <dd>

Reservado. Definido como **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                    |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




