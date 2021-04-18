---
description: Consulta a quantidade de memória temporária que a HAL (camada de abstração de hardware) alocará para seu uso particular.
ms.assetid: 20e3dbef-daf5-487a-8d50-e2ebdb712cc0
title: 'Método IDirect3DVideoDevice9:: GetDXVAInternalInfo (DXVA. h)'
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
ms.openlocfilehash: aa512130b622d192acc37d8c309f462f8ecc87e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780400"
---
# <a name="idirect3dvideodevice9getdxvainternalinfo-method"></a>Método IDirect3DVideoDevice9:: GetDXVAInternalInfo

Consulta a quantidade de memória temporária que a HAL (camada de abstração de hardware) alocará para seu uso particular.

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

*pGuid* 
</dt> <dd>

Ponteiro para um GUID que especifica o perfil de DXVA. Para obter uma lista de perfis com suporte, chame [**IDirect3DVideoDevice9:: GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).

</dd> <dt>

*pUncompData* 
</dt> <dd>

Ponteiro para uma estrutura [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) que especifica o tamanho e o formato de pixel dos dados descompactados.

</dd> <dt>

*pMemoryUsed* 
</dt> <dd>

Recebe a quantidade de memória temporária que o HAL alocará, em bytes.

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

 

 




