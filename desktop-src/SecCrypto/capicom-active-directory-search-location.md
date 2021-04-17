---
description: Indica o local a ser procurado em um repositório de certificados Active Directory.
ms.assetid: 56b9695e-7ab9-405b-9cae-d78c43071186
title: Enumeração de CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: cd630bdc0c09a6bb57a9163ec972451011f3e826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748398"
---
# <a name="capicom_active_directory_search_location-enumeration"></a>\_ \_ \_ Enumeração do local de pesquisa do Active Directory CAPICOM \_

O tipo de enumeração do **local de \_ pesquisa do Active \_ Directory \_ \_ CAPICOM** indica o local a ser procurado em um [*repositório de certificados*](../secgloss/c-gly.md)Active Directory.

## <a name="members"></a>Membros



| Membro                               | DESCRIÇÃO                                  | Valor |
|--------------------------------------|----------------------------------------------|-------|
| **capicote \_ Search \_ any**             | Pesquisa todos os locais disponíveis.<br/> | 0     |
| **CAPICOM de \_ pesquisa do \_ \_ catálogo global** | Pesquisa apenas o catálogo global.<br/> | 1     |
| **CAPICOM de \_ pesquisa de \_ \_ domínio padrão** | Pesquisa apenas o domínio padrão.<br/> | 2     |



## <a name="remarks"></a>Comentários

Esse tipo de enumeração é usado pela seguinte propriedade:

-   [**Settings. ActiveDirectorySearchLocation**](settings-activedirectorysearchlocation.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                |
| parâmetro<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
