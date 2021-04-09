---
description: O Windows Installer organiza uma instalação em todos os conceitos de componentes e recursos.
ms.assetid: c560441e-89c5-4f82-837b-988c3f404d37
title: Componentes e recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b21241c98fbb701bd6a3ef5869045ef8c46da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090943"
---
# <a name="components-and-features"></a>Componentes e recursos

O Windows Installer organiza uma instalação em todos os conceitos de componentes e recursos.

Um recurso faz parte da funcionalidade total do aplicativo que um usuário pode decidir instalar de forma independente. Para obter mais informações, consulte [Windows Installer recursos](windows-installer-features.md).

Um componente é uma parte do aplicativo ou produto a ser instalado. O instalador sempre instala ou remove um componente do computador de um usuário como uma peça coerente. Os componentes geralmente são ocultos do usuário. Quando um usuário seleciona um recurso para instalação, o instalador determina quais componentes devem ser instalados para fornecer esse recurso. Para obter mais informações, consulte [Windows Installer Components](windows-installer-components.md).

Os autores de pacotes de instalação precisam decidir como dividir seu aplicativo em recursos e componentes. A seleção de recursos é determinada principalmente pela funcionalidade do aplicativo da perspectiva do usuário. Como os componentes normalmente devem ser compartilhados entre aplicativos ou até mesmo em todos os produtos, é recomendável que os autores sigam um método padrão para selecionar componentes. Para obter mais informações, consulte [organizando aplicativos em componentes](organizing-applications-into-components.md).

 

 



