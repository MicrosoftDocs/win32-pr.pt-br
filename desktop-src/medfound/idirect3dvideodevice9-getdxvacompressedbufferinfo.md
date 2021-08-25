---
description: Obtém informações sobre os buffers compactados necessários para decodificação acelerada por hardware.
ms.assetid: 5a9fb077-fd79-4faa-a0f8-b3ac987adf36
title: Método IDirect3DVideoDevice9::GetDXVACompressedBufferInfo (Dxva.h)
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
ms.openlocfilehash: efb96ec457cdb81f89982947bf1b9bc40543789b2e9ac253d83c81727f1efae5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942286"
---
# <a name="idirect3dvideodevice9getdxvacompressedbufferinfo-method"></a>Método IDirect3DVideoDevice9::GetDXVACompressedBufferInfo

Obtém informações sobre os buffers compactados necessários para decodificação acelerada por hardware.

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

*Pguid* 
</dt> <dd>

Ponteiro para um GUID que especifica o perfil DXVA. Para obter uma lista de perfis com suporte, chame [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).

</dd> <dt>

*pUncompData* 
</dt> <dd>

Ponteiro para uma [**estrutura DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) que especifica o tamanho e o formato de pixel dos dados descompactados.

</dd> <dt>

*pNumBuffers* 
</dt> <dd>

Na entrada, especifica o número de elementos na *matriz pBufferInfo.* Se *pBufferInfo* for **NULL,** o valor de `*pNumBuffers` deverá ser zero.

Na saída, se *pBufferInfo* for **NULL,** *pNumBuffers* receberá o tamanho da matriz a ser alocada. Caso contrário, *pNumBuffers* receberá o número real de elementos copiados para a *matriz pBufferInfo.*

</dd> <dt>

*pBufferInfo* 
</dt> <dd>

Endereço de uma matriz de estruturas [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) ou **NULL.** Se o valor for não **NULL,** o método copia uma lista de estruturas **DXVACompBufferInfo** para essa matriz. Cada estrutura corresponde a um tipo de buffer de dados compactado que é usado pelo acelerador de vídeo.

De definir todos os elementos da matriz como zero antes de chamar esse método.

Cada índice de matriz corresponde a um dos tipos de superfície DXVA definidos em dxva.h. O acelerador de vídeo retorna uma lista de até entradas da matriz **DXVA \_ NUM TYPES COMP \_ \_ \_ BUFFERS.** Para obter detalhes, consulte a especificação [DXVA 1.0](/windows-hardware/drivers/display/directx-video-acceleration), seção 3.4, "Lista de Descrições do Buffer". Se um tipo de buffer específico não for usado pelo perfil DXVA, a entrada nesse índice conterá zeros para todos os valores.

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

 

 
