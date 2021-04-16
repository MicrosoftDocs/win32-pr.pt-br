---
description: Obtém uma lista de perfis de monitoração de vídeo do DirectX (DXVA) que têm suporte do driver de vídeo.
ms.assetid: 4adbbac2-a25d-4e17-b62e-a02a67dcdbed
title: 'Método IDirect3DVideoDevice9:: GetDXVAGuids (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAGuids
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3ea05af8f27399af38419e177d7bd40b029cd63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765052"
---
# <a name="idirect3dvideodevice9getdxvaguids-method"></a>Método IDirect3DVideoDevice9:: GetDXVAGuids

Obtém uma lista de perfis de monitoração de vídeo do DirectX (DXVA) que têm suporte do driver de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDXVAGuids(
   DWORD *pNumGuids,
   GUID  *pGuids
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pNumGuids* 
</dt> <dd>

Na entrada, especifica o número de elementos na matriz *pGuids* . Se *pGuids* for **NULL**, o valor de `*pNumGuids` deverá ser zero.

Na saída, se *pGuids* for **NULL**, *pNumGuids* receberá o número de perfis de DXVA de modo restrito. Caso contrário, *pNumGuids* receberá o número real de GUIDs que são copiados para a matriz *pGuids* .

</dd> <dt>

*pGuids* 
</dt> <dd>

Endereço de uma matriz de GUIDs ou **NULL**. Se o valor for não **nulo**, a matriz receberá uma lista de GUIDs que especificam perfis de DXVA de modo restrito. Esses GUIDs são definidos em DXVA. h e estão documentados na [especificação dxva 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Chame esse método duas vezes. Na primeira chamada, defina *pGuids* como **nulo**. O parâmetro *pNumGuids* recebe o número de GUIDs de perfil de DXVA. Aloque uma matriz de GUIDs com o tamanho necessário e chame o método novamente. Desta vez, defina *pGuids* como o endereço da matriz. O método preenche a matriz com a lista de GUIDs de perfil de DXVA.

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

 

 
