---
title: Provedores de serviços ADSI
description: Este tópico fornece uma visão geral dos provedores de serviços ADSI fornecidos no servidor.
ms.assetid: 419d7953-a879-4d6c-be74-173d76c3f932
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, provedores de serviços
- ADSI de provedores de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44ba4ebc63338bfb38d2b9d5da1f46e51b31aa8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105756283"
---
# <a name="adsi-service-providers"></a>Provedores de serviços ADSI

A ADSI inclui os provedores de serviços listados na tabela a seguir.



| Provedor de serviços | Descrição                                                                                | Para obter mais informações                                      |
|------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| LDAP<br/>  | Implementação de namespace compatível com o Lightweight Directory Access Protocol.<br/> | [Provedor LDAP ADSI](adsi-ldap-provider.md)<br/>   |
| WinNT<br/> | Implementação de namespace compatível com o Windows.<br/>                               | [Provedor ADSI de WinNT](adsi-winnt-provider.md)<br/> |



 

Outros provedores de serviços são incluídos como parte de produtos diferentes da ADSI. A seguir estão os provedores de serviços ADSI implementados pela Microsoft.



| Provedor de serviços | Para obter mais informações                                                                        |
|------------------|---------------------------------------------------------------------------------------------|
| IIS<br/>   | [Arquitetura do provedor ADSI do IIS](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))<br/> |



 

Os métodos e métodos de propriedade expostos por interfaces ADSI não têm suporte de todos os provedores de serviços. Como os diferentes serviços de diretório variam de acordo com os tipos de objetos e propriedades armazenados, use protocolos diferentes e a autenticação, a ADSI foi projetada para funcionar diretamente com os provedores de serviços com suporte. Portanto, há interfaces, métodos e métodos de propriedade que funcionam com um provedor de serviços, como o LDAP, que podem não funcionar em outro, como o WinNT.

Esta seção contém informações específicas do provedor, como o formato ADsPath, uma lista de objetos ADSI usados para esse provedor de serviços e informações de tipo e sintaxe de dados para os provedores de serviços incluídos na ADSI. Também há uma descrição resumida das interfaces ADSI com suporte de cada provedor incluído na ADSI.

Na ADSI, provedores diferentes são associados a DLLs diferentes. O provedor LDAP está associado a Adsldp.dll, Adsldpc.dll e Adsmsext.dll. O provedor WinNT está associado a Adsnt.dll. O provedor do roteador está associado a Activeds.dll.

> [!Note]  
> Não presuma que os provedores ADSI padrão sejam thread-safe. Os desenvolvedores de aplicativos multithread devem coordenar o acesso entre threads por meio do uso adequado de objetos de sincronização, como semáforos, exclusões mútuas, seções críticas e assim por diante.

 

Para obter mais informações sobre provedores de serviços ADSI, consulte suporte de [roteador](adsi-router.md) e [provedor ADSI de interfaces ADSI](provider-support-of-adsi-interfaces.md).

 

