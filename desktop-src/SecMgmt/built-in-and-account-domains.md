---
description: Explica domínios internos e de conta em sistemas baseados no Windows.
ms.assetid: 306c258b-950e-4506-99e2-67a3714285ff
title: Domínios internos e de conta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d2d4bb18e1ac2ea33aaff008475a44515d9231
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105784135"
---
# <a name="built-in-and-account-domains"></a>Domínios internos e de conta

Os domínios em um sistema baseado no Windows se enquadram nas duas categorias a seguir:

-   [Computadores que não são controladores de domínio](#computers-that-are-not-domain-controllers)
-   [Computadores que são controladores de domínio](#computers-that-are-domain-controllers)

## <a name="computers-that-are-not-domain-controllers"></a>Computadores que não são controladores de domínio

O banco de dados SAM (Gerenciador de contas de segurança) reside em cada computador e gerencia contas para o domínio interno e o domínio da conta.



| Domínio          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Domínio interno | Esse domínio contém grupos locais padrão, como os grupos Administradores e usuários, que são estabelecidos quando o sistema operacional é instalado. O nome desse domínio é uma versão localizada do BUILTIN.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Domínio da conta  | O domínio da conta pode conter contas de usuário, grupo e grupo local. A conta de administrador está nesse domínio. As contas definidas no domínio da conta de uma estação de trabalho ou servidor membro são limitadas a acessar recursos localizados no computador físico onde reside a conta. Em um sistema que não faz parte de uma rede e, portanto, não tem [domínio primário](primary-and-trusted-domains.md), o domínio da conta é usado para armazenar todas as contas que fornecem acesso ao computador. Em um sistema que faz parte de uma rede, o domínio da conta do computador é usado para hospedar contas que não acessam recursos de rede. As contas que exigem acesso à rede devem ser definidas no domínio da conta de um controlador de domínio.<br/> O nome desse domínio é atribuído no momento da instalação do sistema e é determinado pelo nome do computador. Se o nome do computador for alterado, o nome de domínio da conta não será atualizado até que o computador seja reiniciado.<br/> |



 

## <a name="computers-that-are-domain-controllers"></a>Computadores que são controladores de domínio

Os controladores de domínio não têm domínios internos ou de conta. Além disso, em vez de um banco de dados SAM, esses sistemas usam o serviço de diretório do Microsoft Active Directory para armazenar informações de acesso à conta. Para obter mais informações, consulte [Active Directory](/windows/desktop/AD/active-directory-domain-services).

 

