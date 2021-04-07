---
description: Um pacote de 64 bits consiste parcialmente ou totalmente em componentes de Windows Installer de 64 bits.
ms.assetid: 615a5534-7c9e-4240-9a23-35f224122d0e
title: Pacotes de Windows Installer de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b34c8ff7ce4809dc44932cc8a5daa978b6ff66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828100"
---
# <a name="64-bit-windows-installer-packages"></a>Pacotes de Windows Installer de 64 bits

Um pacote de 64 bits consiste parcialmente ou totalmente em componentes de [Windows Installer](windows-installer-components.md) de 64 bits. A lista a seguir identifica os requisitos para cada pacote de Windows Installer de 64 bits:

-   O valor "Intel64" deve ser inserido no campo plataforma da propriedade [**Resumo do modelo**](template-summary.md) se e somente se o pacote for executado em um processador Intel64 (Itanium).
-   O valor "x64" deve ser inserido no campo plataforma da propriedade [**Resumo do modelo**](template-summary.md) se e somente se o pacote for executado em um processador x64.
-   O valor "Arm64" deve ser inserido no campo plataforma da propriedade [**Resumo do modelo**](template-summary.md) se e somente se o pacote for executado em um processador Arm64.
-   A propriedade de [**Resumo contagem de páginas**](page-count-summary.md) deve ser definida como o número inteiro 200 ou maior, porque Windows Installer 2,0 é a versão mínima que é capaz de instalar os componentes da 64 bits. Os pacotes para a plataforma Arm64 exigem um valor de 500 ou superior.
-   Cada componente de Windows Installer de 64 bits no pacote deve incluir o bit **msidbComponentAttributes64bit** na coluna Attributes da [tabela Component](component-table.md).

Para obter mais informações, consulte [Windows Installer em sistemas operacionais de 64 bits](windows-installer-on-64-bit-operating-systems.md) e [pacotes de Windows Installer de 32 bits](32-bit-windows-installer-packages.md).

 

 



