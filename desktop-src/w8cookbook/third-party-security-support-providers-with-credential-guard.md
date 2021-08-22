---
title: Credential Guard e aplicativos de terceiros
description: O Credential Guard não permite que SSPs terceirizados solicitem hashes de senha da LSA.
ms.assetid: DA518005-C603-41CF-BBB9-2B46414653A5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a5c773379e3b7fa52e2095d8db676dddc081e51806fd8f615d2b3a4b744fea95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706746"
---
# <a name="third-party-security-support-providers-with-credential-guard"></a>Provedores de suporte de segurança de terceiros com o Credential Guard

O Credential Guard não permite que SSPs terceirizados solicitem hashes de senha da LSA. No entanto, SSPs e PAs ainda são notificados sobre a senha quando um usuário faz logon e/ou altera sua senha. Qualquer uso de APIs não documentadas dentro de SSPs e PAs personalizados não é permitido.

À medida que a profundidade e a abrangência de proteções fornecidas pelo Credential Guard aumentam, as versões posteriores do Windows 10 com o Credential Guard podem ter impacto em cenários que funcionavam no passado. Por exemplo, o Credential Guard pode bloquear o uso de um determinado tipo de credencial ou componente para impedir que malwares tirem proveito das vulnerabilidades. Portanto, recomendamos que os cenários necessários para as operações em uma organização sejam testados antes da atualização de um dispositivo que tenha o Credential Guard em execução.

Veja [Este artigo](/windows/security/identity-protection/credential-guard/credential-guard) para obter a descrição completa e as atenuações recomendadas.

 

 