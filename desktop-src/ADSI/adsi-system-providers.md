---
title: Provedores de Serviços ADSI
description: Este tópico fornece uma visão geral dos provedores de serviços ADSI fornecidos no servidor.
ms.assetid: 419d7953-a879-4d6c-be74-173d76c3f932
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, Provedores de Serviços
- ADSI de Provedores de Serviços
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e66b90aad4e9fa1a6cf6a2229910257f018a411aa7b11b9accca6fcf96dce39b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962187"
---
# <a name="adsi-service-providers"></a>Provedores de Serviços ADSI

A ADSI inclui os provedores de serviços listados na tabela a seguir.



| Provedor de serviços | Descrição                                                                                | Para obter mais informações                                      |
|------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| LDAP<br/>  | Implementação de namespace compatível com o Lightweight Directory Access Protocol.<br/> | [Provedor ADSI LDAP](adsi-ldap-provider.md)<br/>   |
| Winnt<br/> | Implementação de namespace compatível com Windows.<br/>                               | [Provedor WinNT ADSI](adsi-winnt-provider.md)<br/> |



 

Outros provedores de serviços são incluídos como parte de produtos diferentes da ADSI. A seguir estão os provedores de serviços ADSI implementados pela Microsoft.



| Provedor de serviços | Para obter mais informações                                                                        |
|------------------|---------------------------------------------------------------------------------------------|
| IIS<br/>   | [Arquitetura do provedor ADSI do IIS](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))<br/> |



 

Os métodos e métodos de propriedade expostos por interfaces ADSI não são suportados por todos os provedores de serviços. Como diferentes serviços de diretório variam nos tipos de objetos e propriedades armazenados, usam protocolos diferentes e autenticação, a ADSI foi projetada para funcionar perfeitamente com provedores de serviços com suporte. Portanto, há interfaces, métodos e métodos de propriedade que funcionam com um provedor de serviços, como LDAP, que podem não funcionar em outro, como WinNT.

Esta seção contém informações específicas do provedor, como o formato ADsPath, uma listagem de objetos ADSI usados para esse provedor de serviços e informações de tipo de dados e sintaxe para os provedores de serviços incluídos com ADSI. Também há uma descrição resumida das interfaces ADSI com suporte por cada provedor incluído no ADSI.

No ADSI, diferentes provedores estão associados a diferentes DLLs. O provedor LDAP está associado a Adsldp.dll, Adsldpc.dll e Adsmsext.dll. O provedor WinNT está associado ao Adsnt.dll. O provedor ROUTER está associado a Activeds.dll.

> [!Note]  
> Não suponha que os provedores ADSI padrão sejam thread-safe. Os desenvolvedores de aplicativos multithread devem coordenar o acesso entre threads por meio do uso adequado de objetos de sincronização, como semáforos, mutexes, seções críticas e assim por diante.

 

Para obter mais informações sobre provedores de serviços [ADSI,](adsi-router.md) consulte Suporte de roteador ADSI e [provedor de interfaces ADSI](provider-support-of-adsi-interfaces.md).

 

