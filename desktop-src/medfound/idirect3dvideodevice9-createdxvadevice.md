---
description: Cria um dispositivo de decodificador DXVA (DirectX Video Acceleration).
ms.assetid: aeebf65f-1bde-4a33-87cd-25c62dcc0248
title: 'Método IDirect3DVideoDevice9:: CreateDXVADevice (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateDXVADevice
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 4f70f976487db270145c8587107499f3c4e84ad85dacf99bec21050a2684b723
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555726"
---
# <a name="idirect3dvideodevice9createdxvadevice-method"></a>Método IDirect3DVideoDevice9:: CreateDXVADevice

Cria um dispositivo de decodificador DXVA (DirectX Video Acceleration).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateDXVADevice(
   GUID                 *pGuid,
   DXVAUncompDataInfo   *pUncompData,
   LPVOID               pData,
   DWORD                DataSize,
   IDirect3DDXVADevice9 **ppDXVADevice
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pGuid* 
</dt> <dd>

Ponteiro para um GUID que especifica o dispositivo a ser criado.

</dd> <dt>

*pUncompData* 
</dt> <dd>

Ponteiro para uma estrutura [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) que especifica o formato da imagem descompactada.

</dd> <dt>

*pData* 
</dt> <dd>

Ponteiro para uma estrutura **DXVA \_ ConnectMode** que especifica o modo DXVA e o perfil restrito.

</dd> <dt>

*DataSize* 
</dt> <dd>

Tamanho da estrutura **DXVA \_ ConnectMode** , em bytes.

</dd> <dt>

*ppDXVADevice* 
</dt> <dd>

Recebe um ponteiro para a interface [**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md) . O chamador deve liberar a interface.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                    |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




