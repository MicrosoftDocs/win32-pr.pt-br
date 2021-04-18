---
description: Consulta o status de leitura/gravação de uma superfície de decodificação de aceleração de vídeo do DirectX (DXVA).
ms.assetid: 8a4c3173-5911-49ec-8cb8-e30f96a4f1c9
title: 'Método IDirect3DDXVADevice9:: QueryStatus (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.QueryStatus
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: ae2b16ef27b1e172b7927652304104563e120709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814467"
---
# <a name="idirect3ddxvadevice9querystatus-method"></a>Método IDirect3DDXVADevice9:: QueryStatus

Consulta o status de leitura/gravação de uma superfície de decodificação de aceleração de vídeo do DirectX (DXVA).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT QueryStatus(
   IDirect3DSurface9 *pSurface,
   DWORD             Flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSurface* 
</dt> <dd>

Ponteiro para a interface **IDirect3DSurface9** da superfície a ser consultada.

</dd> <dt>

*Sinalizadores* 
</dt> <dd>

Especifica o tipo de consulta a ser executada.



| Valor                                                                                                                             | Significado                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="0x00"></span><span id="0X00"></span><dl> <dt>**0x00**</dt> </dl> | Teste se a superfície é segura para ser usada para gravação.<br/> |
| <span id="0x01"></span><span id="0X01"></span><dl> <dt>**0x01**</dt> </dl> | Teste se a superfície é segura para ser usada para leitura.<br/> |



 

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

[**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




