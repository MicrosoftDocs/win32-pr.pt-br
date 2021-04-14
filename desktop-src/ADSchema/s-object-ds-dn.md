---
title: Sintaxe de objeto (DS-DN)
description: Cadeia de caracteres que contém um DN (nome distinto).
ms.assetid: 089104c4-ff82-49ea-a8db-a6dadc3a18bc
ms.tgt_platform: multiple
keywords:
- Esquema de sintaxe de objeto (DS-DN) do AD
topic_type:
- apiref
api_name:
- Object(DS-DN)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45154985fa7fbfc4d95d563196357d43eac2ea72
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104499874"
---
# <a name="objectds-dn-syntax"></a>Sintaxe de objeto (DS-DN)

Cadeia de caracteres que contém um DN (nome distinto). Para atributos com essa sintaxe, Active Directory manipula valores de atributo como referências ao objeto identificado pelo DN e atualiza automaticamente o valor se o objeto for movido ou renomeado. Para consultas que incluem atributos de sintaxe de DN em um filtro, especifique nomes distintos completos. Não há suporte para caracteres curinga (por exemplo, CN = João \* ).



| Entrada | Valor |
|--------------|------------------------------------------------------------------------|
| Nome         | Objeto (DS-DN)                                                          |
| ID da sintaxe    | 2.5.5.1                                                                |
| ID DO OM        | 127                                                                    |
| Tipo de MAPI    | OBJECT                                                                 |
| Tipo de ADS     | \_cadeia de \_ caracteres DN ADSTYPE                                                    |
| Tipo de variante | VT \_ BSTR                                                               |
| Tipo SDS     | [System.String](/dotnet/api/system.string) |



## <a name="see-also"></a>Confira também

<dl> <dt>

[System.String](/dotnet/api/system.string)
</dt> </dl>

 

 
