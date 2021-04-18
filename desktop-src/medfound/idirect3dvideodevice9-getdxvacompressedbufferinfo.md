---
description: Obtém informações sobre os buffers compactados necessários para a decodificação acelerada por hardware.
ms.assetid: 5a9fb077-fd79-4faa-a0f8-b3ac987adf36
title: 'Método IDirect3DVideoDevice9:: GetDXVACompressedBufferInfo (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVACompressedBufferInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 2bd2dcdd931ac8778e4f1c11f1479fe54e23d1b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105815514"
---
# <a name="idirect3dvideodevice9getdxvacompressedbufferinfo-method"></a>Método IDirect3DVideoDevice9:: GetDXVACompressedBufferInfo

Obtém informações sobre os buffers compactados necessários para a decodificação acelerada por hardware.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDXVACompressedBufferInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pNumBuffers,
   DXVACompBufferInfo *pBufferInfo
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

*pNumBuffers* 
</dt> <dd>

Na entrada, especifica o número de elementos na matriz *pBufferInfo* . Se *pBufferInfo* for **NULL**, o valor de `*pNumBuffers` deverá ser zero.

Na saída, se *pBufferInfo* for **NULL**, *pNumBuffers* receberá o tamanho da matriz a ser alocada. Caso contrário, *pNumBuffers* receberá o número real de elementos que são copiados para a matriz *pBufferInfo* .

</dd> <dt>

*pBufferInfo* 
</dt> <dd>

Endereço de uma matriz de estruturas [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) ou **NULL**. Se o valor for não **nulo**, o método copiará uma lista de estruturas **DXVACompBufferInfo** para essa matriz. Cada estrutura corresponde a um tipo de buffer de dados compactado que é usado pelo acelerador de vídeo.

Defina todos os elementos da matriz como zero antes de chamar esse método.

Cada índice de matriz corresponde a um dos tipos de superfície de DXVA definidos em DXVA. h. O acelerador de vídeo retorna uma lista de até as entradas de matriz de **\_ \_ \_ \_ buffers de comp. de tipos de número DXVA** . Para obter detalhes, consulte a [especificação de DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration), seção 3,4, "lista de descrição de buffer". Se um determinado tipo de buffer não for usado pelo perfil de DXVA, a entrada nesse índice conterá zeros para todos os valores.

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

 

 
