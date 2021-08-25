---
description: O editor de controle de acesso pode incluir uma página de propriedades proprietário que permite que o usuário altere um proprietário de objetos. Para obter mais informações sobre um proprietário de objetos, consulte Proprietário de um novo objeto e Tomada de propriedade de objeto em C++.
ms.assetid: b0c421db-450e-4030-98e9-e062202e482c
title: Página de propriedades do proprietário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b67b3707017aa8073cfdf4f5ca64340eda74a640bc604a0bd382b7cf2ebe122e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907656"
---
# <a name="owner-property-page"></a>Página de propriedades do proprietário

O editor de controle de acesso pode incluir uma página de propriedades proprietário que permite que o usuário altere o proprietário de um objeto. Para obter mais informações sobre o proprietário de um objeto, consulte [Proprietário de um](owner-of-a-new-object.md) novo objeto e Tomada de propriedade de objeto em [C++.](taking-object-ownership-in-c--.md)

A **página de** propriedades Proprietário está na folha [de](advanced-security-property-sheet.md) propriedades de segurança avançada exibida quando o usuário clica no **botão** Avançado na página de propriedades de [segurança básica](basic-security-property-page.md). Para incluir  a página de propriedades Proprietário, de definir os sinalizadores SI ADVANCED e SI EDIT OWNER na estrutura SI OBJECT INFO retornada pela implementação \_ de \_ \_ [**ISecurityInformation::GetObjectInformation.**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) [**\_ \_**](/windows/desktop/api/Aclui/ns-aclui-si_object_info)

 

 
