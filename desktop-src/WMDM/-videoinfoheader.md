---
title: _VIDEOINFOHEADER estrutura
description: A estrutura VIDEOINFOHEADER contém informações sobre um fluxo de vídeo e inclui uma estrutura \_ \_ BITMAPINFOHEADER que define o formato de um quadro individual.
ms.assetid: 5a39d66e-8dbc-4572-8370-14f722b6c906
keywords:
- _VIDEOINFOHEADER estrutura windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- _VIDEOINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b00c641f0fb9a9f68217de8a21a732b4b45a8e4417104be981ffd90161f7340
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586796"
---
# <a name="_videoinfoheader-structure"></a>\_Estrutura VIDEOINFOHEADER

A **\_ estrutura VIDEOINFOHEADER** contém informações sobre um fluxo de vídeo e inclui uma estrutura **\_ BITMAPINFOHEADER** que define o formato de um quadro individual.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _tagVIDEOINFOHEADER {
  RECT             rcSource;
  RECT             rcTarget;
  DWORD            dwBitRate;
  DWORD            dwBitErrorRate;
  REFERENCE_TIME   AvgTimePerFrame;
  BITMAPINFOHEADER bmiHeader;
} _VIDEOINFOHEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**Rcsource**
</dt> <dd>

**Estrutura RECT** que especifica a janela de vídeo de origem.

</dd> <dt>

**Rctarget**
</dt> <dd>

**Estrutura RECT** que especifica a janela de vídeo de destino.

</dd> <dt>

**dwBitRate**
</dt> <dd>

**Valor DWORD** que especifica a taxa de dados aproximada do fluxo de vídeo, em bits por segundo.

</dd> <dt>

**dwBitErrorRate**
</dt> <dd>

**Valor DWORD** que especifica a taxa de erro de dados do fluxo de vídeo, em erros de bit por segundo.

</dd> <dt>

**AvgTimePerFrame**
</dt> <dd>

**REFERÊNCIA \_ Valor** TIME que especifica o tempo médio de exibição do quadro de vídeo, em unidades de 100 nanossegundos.

</dd> <dt>

**Bmiheader**
</dt> <dd>

Estrutura Win32 **\_ BITMAPINFOHEADER** que contém informações de cor e dimensão para o bitmap da imagem de vídeo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Bitmapinfoheader**](-bitmapinfoheader.md)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





