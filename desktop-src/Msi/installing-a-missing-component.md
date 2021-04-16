---
description: Você pode usar o Windows Installer para detectar componentes ou arquivos ausentes e, em seguida, reinstalar os recursos que contêm os componentes ausentes.
ms.assetid: b197c9d0-fcc2-4ca7-a870-e1af82343455
title: Instalando um componente ausente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9bbfd38517e850a7f4e83c9c84075d92fea2290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752248"
---
# <a name="installing-a-missing-component"></a>Instalando um componente ausente

Você pode usar o Windows Installer para detectar componentes ou arquivos ausentes e, em seguida, reinstalar os recursos que contêm os componentes ausentes. Como o instalador instala recursos e não componentes, ele deve primeiro resolver a qual componente um arquivo ausente pertence e, em seguida, instalar o recurso que contém o componente. Se mais de um recurso estiver vinculado ao componente, o instalador instalará o recurso que requer o menor espaço em disco.

Se você chamar [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha), poderá verificar se o arquivo de chave de um componente está presente. No entanto, ainda é possível que outros arquivos pertencentes ao componente estejam ausentes. Nesse cenário, chame [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea). O instalador, em seguida, resolve para qual componente o arquivo pertence e instala o recurso que está vinculado ao componente que requer o menor espaço em disco.

Se a função [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) falhar inesperadamente, você deverá instalar os componentes ausentes.

O procedimento a seguir mostra como instalar componentes ausentes.

**Para detectar e instalar um componente ausente**

1.  Chame [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) para verificar se o arquivo de chave de um componente está presente. No entanto, mesmo que o arquivo de chave do componente esteja presente, ainda é possível que outros arquivos pertencentes ao componente estejam ausentes.
2.  Chame a função [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) se o recurso associado ao componente for desconhecido.
3.  Chame a função [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) ou [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) se o recurso associado ao componente for conhecido.
4.  Chame [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) se um aplicativo não puder abrir um arquivo.

 

 



