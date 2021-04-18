---
description: Este exemplo ilustra como localizar o pacote de Windows Installer descrito em um exemplo de instalação. O pacote de instalação original é alterado de uma versão em inglês para o idioma francês.
ms.assetid: b14787fe-3179-47d7-8a15-da45987d613f
title: Um exemplo de localização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d5ae0b04e65383d665e2532d45f0cc2eed856a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768490"
---
# <a name="a-localization-example"></a>Um exemplo de localização

Este exemplo ilustra como localizar o pacote de Windows Installer descrito em [um exemplo de instalação](an-installation-example.md). O pacote de instalação original é alterado de uma versão em inglês para o idioma francês.

O exemplo de localização tem as seguintes especificações:

-   A interface do usuário de instalação do aplicativo MNP2000 deve ser alterada de Inglês para francês.
-   A versão em francês do MNP2000 inclui arquivos de Readme.txt e Help.txt escritos no idioma francês.
-   A versão em francês inclui uma lista de agentes de viagem na França que podem fornecer tíquetes para a arena do Parque vermelho. Essa lista (fornecida como um novo arquivo, Fre.txt) não faz parte da versão em inglês.

O procedimento geral para localizar uma instalação é descrito na seção [localizando um pacote de Windows Installer](localizing-a-windows-installer-package.md).

Copie a versão em inglês do MNP2000.msi e todos os arquivos de origem descritos em [planejando a instalação](planning-the-installation.md) em uma nova pasta. Altere o nome do MNP2000.msi na pasta para MNPFren.msi. Nas seções a seguir, você modificará essa cópia para localizar o aplicativo em francês.

[Continuar](checking-the-installation-database-code-page.md)

 

 



