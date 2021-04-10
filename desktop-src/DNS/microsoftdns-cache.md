---
title: Classe MicrosoftDNS_Cache
description: A \_ classe de cache MicrosoftDNS descreve um cache existente em um servidor DNS.
ms.assetid: 139406eb-70f2-4614-9662-703ada032298
keywords:
- MicrosoftDNS_Cache de classe de DNS
- MicrosoftDNS_Cache de classe de DNS, descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_Cache
- MicrosoftDNS_Cache.ClearCache
- MicrosoftDNS_Cache.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e55bda9c38d889fe1b84ef28432b18e5724af09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009378"
---
# <a name="microsoftdns_cache-class"></a>\_Classe de cache MicrosoftDNS

A classe de **\_ cache MicrosoftDNS** descreve um cache existente em um servidor DNS. Essa classe simplifica a visualização da contenção de objetos DNS, em vez de representar um objeto real. A classe de **\_ cache MicrosoftDNS** é um contêiner para os registros de recursos armazenados em cache pelo servidor DNS. Não confunda isso com um arquivo de cache que contém dicas de raiz.

Cada instância do **\_ cache MicrosoftDNS** de classe deve ser atribuída a exatamente um servidor DNS. Ele pode ser associado a várias instâncias do [**\_ domínio MicrosoftDNS**](microsoftdns-domain.md) ou [**classes \_ MicrosoftDNS ResourceRecord**](microsoftdns-resourcerecord.md) .

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MicrosoftDNS_Cache : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>Membros

A classe de **\_ cache MicrosoftDNS** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A classe de **\_ cache MicrosoftDNS** tem esses métodos.



| Método                   | Descrição                                                                                     |
|:-------------------------|:------------------------------------------------------------------------------------------------|
| **ClearCache**           | Limpa o cache do servidor DNS dos registros de recursos. <br/> Qualificadores: implementados<br/> |
| **Getdistinguiname** | Recupera o nome distinto da zona. <br/> Qualificadores: implementados<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Domínio MicrosoftDNS**](microsoftdns-domain.md)
</dt> <dt>

[**Método ClearCache da classe de \_ cache MicrosoftDNS**](microsoftdns-cache-clearcache.md)
</dt> <dt>

[**Método getdistinguiname da classe de \_ cache MicrosoftDNS**](microsoftdns-cache-getdistinguishedname.md)
</dt> </dl>

 

 





