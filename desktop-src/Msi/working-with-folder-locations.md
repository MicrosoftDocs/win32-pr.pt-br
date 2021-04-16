---
description: Use essas funções para localizar a origem ou o destino de uma pasta especificada na tabela de diretórios de um banco de dados Windows Installer.
ms.assetid: 8f9971da-cca8-4623-bdd2-079c4f4859f9
title: Trabalhando com locais de pasta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22485f7bf0ae2a680c9a0bf52eb9fe62858acf09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752432"
---
# <a name="working-with-folder-locations"></a>Trabalhando com locais de pasta

Use as seguintes funções para localizar a origem ou o destino de uma pasta especificada na [tabela de diretórios](directory-table.md):

-   Obtenha o caminho da pasta de origem especificada chamando a função [**MsiGetSourcePath**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha) .
-   Obtenha o caminho da pasta de destino especificada chamando a função [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) .
-   Altere o local de destino de uma pasta com a função [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) .

 

 



