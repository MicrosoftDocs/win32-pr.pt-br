---
title: Nomes de Entidade de Serviço
description: Um SPN (nome da entidade de serviço) é um identificador exclusivo de uma instância de serviço.
ms.assetid: 54b02853-4097-4e37-b7a2-6b5cfd168ece
ms.tgt_platform: multiple
keywords:
- Nomes de Entidade de Serviço
- SPN consulte nomes da entidade de serviço
- ANÚNCIO do nome da entidade de serviço
- ANÚNCIO do nome da entidade de serviço, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa34b7d90803a324faced7d67b56c0b6a1f13af
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823629"
---
# <a name="service-principal-names"></a>Nomes de Entidade de Serviço

Um SPN (nome da entidade de serviço) é um identificador exclusivo de uma instância de serviço. Os SPNs são usados pela [autenticação Kerberos](mutual-authentication-using-kerberos.md) para associar uma instância de serviço a uma conta de logon de serviço. Isso permite que um aplicativo cliente solicite que o serviço autentique uma conta mesmo que o cliente não tenha o nome da conta.

Se você instalar várias instâncias de um serviço em computadores em uma floresta, cada instância deverá ter seu próprio SPN. Uma determinada instância de serviço pode ter vários SPNs se houver vários nomes que os clientes podem usar para autenticação. Por exemplo, um SPN sempre inclui o nome do computador host no qual a instância de serviço está em execução, portanto, uma instância de serviço pode registrar um SPN para cada nome ou alias de seu host. Para obter mais informações sobre o formato SPN e compor um SPN exclusivo, consulte [formatos de nome para SPNs exclusivos](name-formats-for-unique-spns.md).

Antes que o serviço de autenticação Kerberos possa usar um SPN para autenticar um serviço, o SPN deve ser registrado no objeto de conta que a instância de serviço usa para fazer logon. Um determinado SPN pode ser registrado em apenas uma conta. Para serviços Win32, um instalador de serviço especifica a conta de logon quando uma instância do serviço é instalada. Em seguida, o instalador compõe os SPNs e os grava como uma propriedade do objeto Account no Active Directory Domain Services. Se a conta de logon de uma instância de serviço for alterada, os SPNs deverão ser registrados novamente na nova conta. Para obter mais informações, consulte [como um serviço registra seus SPNs](how-a-service-registers-its-spns.md).

Quando um cliente deseja se conectar a um serviço, ele localiza uma instância do serviço, compõe um SPN para essa instância, conecta-se ao serviço e apresenta o SPN para autenticação do serviço. Para obter mais informações, consulte [como os clientes compõem o SPN de um serviço](how-clients-compose-a-serviceampaposs-spn.md).

## <a name="in-this-section"></a>Nesta seção

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Formatos de nome para SPNs exclusivos](name-formats-for-unique-spns.md)
</dt> <dt>

[Como um serviço compõe seus SPNs](how-a-service-composes-its-spns.md)
</dt> <dt>

[Como um serviço registra seus SPNs](how-a-service-registers-its-spns.md)
</dt> <dt>

[Como os clientes compõem o SPN de um serviço](how-clients-compose-a-serviceampaposs-spn.md)
</dt> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O que é um SPN e por que você deve se importar?](/archive/blogs/autz_auth_stuff/what-is-a-spn-and-why-should-you-care)
</dt> <dt>

[Autenticação mútua usando Kerberos](mutual-authentication-using-kerberos.md)
</dt> </dl>

 

 