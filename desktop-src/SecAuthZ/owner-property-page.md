---
description: O editor de controle de acesso pode incluir uma página de propriedades de proprietário que permite ao usuário alterar um proprietário de objetos. Para obter mais informações sobre um proprietário de objetos, consulte proprietário de um novo objeto e tirando a propriedade do objeto em C++.
ms.assetid: b0c421db-450e-4030-98e9-e062202e482c
title: Página de propriedades do proprietário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cee9d5c276071674ec274c9955a2e8c5cd5a856a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091761"
---
# <a name="owner-property-page"></a>Página de propriedades do proprietário

O editor de controle de acesso pode incluir uma página de propriedades de proprietário que permite ao usuário alterar o proprietário de um objeto. Para obter mais informações sobre o proprietário de um objeto, consulte [proprietário de um novo objeto](owner-of-a-new-object.md) e [tirando a propriedade do objeto em C++](taking-object-ownership-in-c--.md).

A página de propriedades do **proprietário** está na [folha de propriedades segurança avançada](advanced-security-property-sheet.md) exibida quando o usuário clica no botão **avançado** na página de [Propriedades de segurança básica](basic-security-property-page.md). Para incluir a página de propriedades do **proprietário** , defina os \_ sinalizadores do proprietário avançado e de edição do si \_ \_ na estrutura de [**\_ \_ informações do objeto si**](/windows/desktop/api/Aclui/ns-aclui-si_object_info) retornada pela implementação de [**ISecurityInformation:: GetObjectInformation**](/windows/win32/api/aclui/nf-aclui-isecurityinformation-getobjectinformation) .

 

 
