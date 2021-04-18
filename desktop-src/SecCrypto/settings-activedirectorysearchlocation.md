---
description: Define ou recupera o local de pesquisa do Active Directory.
ms.assetid: 43320799-1c01-4e09-bed9-f3576baadcce
title: Propriedade Settings. ActiveDirectorySearchLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.ActiveDirectorySearchLocation
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d218b3d589b76980d468395a39452613aa57ada5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753395"
---
# <a name="settingsactivedirectorysearchlocation-property"></a>Propriedade Settings. ActiveDirectorySearchLocation

\[A propriedade **ActiveDirectorySearchLocation** está disponível para uso nos sistemas operacionais especificados na seção requisitos.\]

A propriedade **ActiveDirectorySearchLocation** define ou recupera o local de pesquisa Active Directory.

## <a name="syntax"></a>Syntax


```VB
Settings.ActiveDirectorySearchLocation As CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
```



## <a name="property-value"></a>Valor da propriedade

Um valor da enumeração [**de \_ \_ local de \_ pesquisa \_ do Active Directory CAPICOM**](capicom-active-directory-search-location.md) que especifica o local de pesquisa. O valor padrão é capicote \_ Search \_ any. A tabela a seguir mostra os valores possíveis.



| Valor                                                                                                                                                                                                           | Significado                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="CAPICOM_SEARCH_ANY"></span><span id="capicom_search_any"></span><dl> <dt>**capicote \_ Search \_ any**</dt> </dl>                                   | Pesquisar todos os locais disponíveis.<br/> |
| <span id="CAPICOM_SEARCH_DEFAULT_DOMAIN"></span><span id="capicom_search_default_domain"></span><dl> <dt>**CAPICOM de \_ pesquisa de \_ \_ domínio padrão**</dt> </dl> | Pesquise somente o domínio padrão.<br/> |
| <span id="CAPICOM_SEARCH_GLOBAL_CATALOG"></span><span id="capicom_search_global_catalog"></span><dl> <dt>**CAPICOM de \_ pesquisa do \_ \_ catálogo global**</dt> </dl> | Pesquise somente o catálogo global.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configurações**](settings.md)
</dt> </dl>

 

 




