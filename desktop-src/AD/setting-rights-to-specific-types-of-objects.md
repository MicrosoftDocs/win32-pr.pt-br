---
title: Definindo direitos para tipos específicos de objetos
description: O procedimento a seguir mostra como definir uma ACE que pode ser herdada somente por uma classe específica de objetos.
ms.assetid: 42712458-69c7-4fe1-bfb3-b3fb28092a56
ms.tgt_platform: multiple
keywords:
- definindo direitos para tipos de objetos AD
- AD de objetos, definindo direitos para
- Active Directory, usando, segurança, definindo direitos para tipos de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f44cfbe753e6f92787f8269eab1f4eab4c2e98
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917102"
---
# <a name="setting-rights-to-specific-types-of-objects"></a>Definindo direitos para tipos específicos de objetos

O procedimento a seguir mostra como definir uma ACE que pode ser herdada somente por uma classe específica de objetos.

 **Para definir uma ACE que pode ser herdada somente por uma classe específica de objetos**

1.  Defina a propriedade [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como **ADS \_ AceType \_ acesso \_ de \_ objeto permitido** ou o **\_ objeto ADS AceType \_ acesso \_ negado \_**.
2.  Defina a propriedade [**IADsAccessControlEntry. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para incluir o \_ sinalizador de Ace ACEFLAG do ADS \_ \_ .
3.  Defina a propriedade [**IADsAccessControlEntry. InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) como o **schemaIDGUID** da classe de objeto que pode herdar a Ace.
4.  Defina a propriedade [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para **o \_ tipo de \_ objeto herdado sinalizador ADS \_ \_ presente**.

> [!IMPORTANT]
> Defina **ADS \_ ACEFLAG \_ INHERIT \_ Ace** para fazer com que a Ace seja herdada. Além disso, você deve definir **ADS \_ ACEFLAG \_ herdar \_ somente \_ Ace** se o tipo de objeto ao qual essa Ace se aplica não corresponder ao tipo de objeto do contêiner onde a ACE é especificada. Se isso não for feito, a ACE também entrará em vigor no contêiner e poderá conceder direitos não pretendidos.

 

Para obter mais informações e exemplos de código que podem ser usados para definir esse tipo de ACE, consulte [código de exemplo para definir uma ACE em um objeto de diretório](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 