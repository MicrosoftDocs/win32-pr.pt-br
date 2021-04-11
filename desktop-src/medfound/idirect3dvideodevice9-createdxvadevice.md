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
ms.openlocfilehash: 50ce7cee350479f4286921b6cdf69b319033c721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090967"
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

 

 




