---
title: Sintaxe de Object(DS-DN)
description: Cadeia de caracteres que contém um DN (nome diferenciado).
ms.assetid: 089104c4-ff82-49ea-a8db-a6dadc3a18bc
ms.tgt_platform: multiple
keywords:
- Esquema do AD de sintaxe object(DS-DN)
topic_type:
- apiref
api_name:
- Object(DS-DN)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0c9adf4138de56d90ac89743c3b428a1f25b45027bc19f0b5dccc2e005b143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835679"
---
# <a name="objectds-dn-syntax"></a>Sintaxe de Object(DS-DN)

Cadeia de caracteres que contém um DN (nome diferenciado). Para atributos com essa sintaxe, o Active Directory trata valores de atributo como referências ao objeto identificado pelo DN e atualiza automaticamente o valor se o objeto for movido ou renomeado. Para consultas que incluem atributos de sintaxe DN em um filtro, especifique nomes diferenciados completos. Não há suporte para curingas (por exemplo, cn=John \* ).



| Entrada | Valor |
|--------------|------------------------------------------------------------------------|
| Nome         | Object(DS-DN)                                                          |
| ID da sintaxe    | 2.5.5.1                                                                |
| OM ID        | 127                                                                    |
| Tipo MAPI    | OBJECT                                                                 |
| Tipo ADS     | ADSTYPE \_ DN \_ STRING                                                    |
| Tipo de variante | VT \_ BSTR                                                               |
| Tipo de SDS     | [System.String](/dotnet/api/system.string) |



## <a name="see-also"></a>Confira também

<dl> <dt>

[System.String](/dotnet/api/system.string)
</dt> </dl>

 

 
