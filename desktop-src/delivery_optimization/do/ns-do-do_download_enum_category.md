---
title: DO_DOWNLOAD_ENUM_CATEGORY estrutura
description: Usado por **IDOManager::EnumDownloads** para filtrar a enumeração downloads pelo valor da propriedade específica.
keywords:
- DO_DOWNLOAD_ENUM_CATEGORY estrutura
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
ms.openlocfilehash: 32bdc7ca9a84bfe87ff453d34c4ecff57a8dabf5f67b21cc0d54ba079efd1578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543750"
---
# <a name="do_download_enum_category-structure"></a>DO_DOWNLOAD_ENUM_CATEGORY estrutura

A **DO_DOWNLOAD_ENUM_CATEGORY** é usada por **IDOManager::EnumDownloads** para filtrar a enumeração downloads pelo valor da propriedade específica.

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

O nome da propriedade a ser usado para a enumeração de download. Essas propriedades têm suporte para fins de enumeração.
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
| **Cliente mínimo com suporte** | \[Windows 10, versão 1809 Somente aplicativos Win32\] |
| **Servidor mínimo com suporte** | Windows Servidor, versão 1809 \[ Somente aplicativos Win32\] |
| **Cabeçalho** | Do.h |
