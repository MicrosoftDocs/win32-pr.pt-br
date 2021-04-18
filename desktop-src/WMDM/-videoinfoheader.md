---
title: Estrutura de _VIDEOINFOHEADER
description: A \_ estrutura VIDEOINFOHEADER contém informações sobre um fluxo de vídeo e inclui uma \_ estrutura BITMAPINFOHEADER que define o formato de um quadro individual.
ms.assetid: 5a39d66e-8dbc-4572-8370-14f722b6c906
keywords:
- Estrutura de _VIDEOINFOHEADER Windows Media Gerenciador de Dispositivos
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
ms.openlocfilehash: a5b389c5c82296e95ecfb3900518af4a2c7ddd7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813400"
---
# <a name="_videoinfoheader-structure"></a>\_Estrutura VIDEOINFOHEADER

A estrutura **\_ VIDEOINFOHEADER** contém informações sobre um fluxo de vídeo e inclui uma estrutura **\_ BITMAPINFOHEADER** que define o formato de um quadro individual.

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

**rcSource**
</dt> <dd>

A estrutura **Rect** que especifica a janela de vídeo de origem.

</dd> <dt>

**rcTarget**
</dt> <dd>

A estrutura **Rect** que especifica a janela de vídeo de destino.

</dd> <dt>

**dwBitRate**
</dt> <dd>

Valor **DWORD** que especifica a taxa aproximada de dados do fluxo de vídeo, em bits por segundo.

</dd> <dt>

**dwBitErrorRate**
</dt> <dd>

Valor **DWORD** que especifica a taxa de erros de dados do fluxo de vídeo, erros de bit por segundo.

</dd> <dt>

**AvgTimePerFrame**
</dt> <dd>

**Referência \_ do** Valor de tempo que especifica o tempo médio de exibição do quadro de vídeo, em unidades de 100 nanossegundos.

</dd> <dt>

**bmiHeader**
</dt> <dd>

Estrutura **\_ BITMAPINFOHEADER** do Win32 que contém informações de cor e dimensão para o bitmap de imagem de vídeo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_BITMAPINFOHEADER**](-bitmapinfoheader.md)
</dt> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

 





