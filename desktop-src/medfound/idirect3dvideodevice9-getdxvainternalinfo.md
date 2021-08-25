---
description: Consultas para a quantidade de memória de rascunho que a CAMADA de abstração de hardware (HAL) alocará para seu uso privado.
ms.assetid: 20e3dbef-daf5-487a-8d50-e2ebdb712cc0
title: Método IDirect3DVideoDevice9::GetDXVAInternalInfo (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAInternalInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: dd15dfdbd35db56262487482e811210970852dcee4e791d710e0551b84e9e620
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777206"
---
# <a name="idirect3dvideodevice9getdxvainternalinfo-method"></a>Método IDirect3DVideoDevice9::GetDXVAInternalInfo

Consultas para a quantidade de memória de rascunho que a CAMADA de abstração de hardware (HAL) alocará para seu uso privado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDXVAInternalInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pMemoryUsed
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pguid* 
</dt> <dd>

Ponteiro para um GUID que especifica o perfil DXVA. Para obter uma lista de perfis com suporte, chame [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).

</dd> <dt>

*pUncompData* 
</dt> <dd>

Ponteiro para uma [**estrutura DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) que especifica o tamanho e o formato de pixel dos dados descompactados.

</dd> <dt>

*pMemoryUsed* 
</dt> <dd>

Recebe a quantidade de memória de rascunho que o HAL alocará, em bytes.

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

 

 




