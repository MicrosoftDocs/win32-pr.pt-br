---
title: Estrutura de DO_DOWNLOAD_ENUM_CATEGORY
description: 'Usado por **IDOManager:: EnumDownloads** para filtrar a enumeração de downloads pelo valor da propriedade específica.'
keywords:
- Estrutura de DO_DOWNLOAD_ENUM_CATEGORY
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_ENUM_CATEGORY
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a78c94cd9d8854453517976300e12a031f65b8cb
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "105798307"
---
# <a name="do_download_enum_category-structure"></a>Estrutura de DO_DOWNLOAD_ENUM_CATEGORY

A estrutura de **DO_DOWNLOAD_ENUM_CATEGORY** é usada por **IDOManager:: EnumDownloads** para filtrar a enumeração de downloads pelo valor da propriedade específica.

## <a name="syntax"></a>Sintaxe
```cpp
typedef struct _DO_DOWNLOAD_ENUM_CATEGORY
{
  DODownloadProperty Property;
  LPCWSTR Value;
} DO_DOWNLOAD_ENUM_CATEGORY;
```

## <a name="members"></a>Membros

`Property`

O nome da propriedade a ser usada para a enumeração de download. Essas propriedades têm suporte para fins de enumeração.
- **DODownloadProperty_Id**
- **DODownloadProperty_Uri**
- **DODownloadProperty_ContentId**
- **DODownloadProperty_DisplayName**
- **DODownloadProperty_LocalPath**

`Value`

O valor da propriedade.

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo com suporte** | Somente aplicativos do Windows 10, versão 1809 \[ Win32\] |
| **Servidor mínimo com suporte** | Somente aplicativos do Windows Server, versão 1809 \[ Win32\] |
| **Cabeçalho** | Do. h |
