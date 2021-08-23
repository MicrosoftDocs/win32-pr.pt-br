---
description: você pode usar o Windows Installer para detectar componentes ou arquivos ausentes e, em seguida, reinstalar os recursos que contêm os componentes ausentes.
ms.assetid: b197c9d0-fcc2-4ca7-a870-e1af82343455
title: Instalando um componente ausente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e788cad738d46d35a7ac0948be2e2e2d6ede4347eec424fb24cf17571e3a59f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828786"
---
# <a name="installing-a-missing-component"></a>Instalando um componente ausente

você pode usar o Windows Installer para detectar componentes ou arquivos ausentes e, em seguida, reinstalar os recursos que contêm os componentes ausentes. Como o instalador instala recursos e não componentes, ele deve primeiro resolver a qual componente um arquivo ausente pertence e, em seguida, instalar o recurso que contém o componente. Se mais de um recurso estiver vinculado ao componente, o instalador instalará o recurso que requer o menor espaço em disco.

Se você chamar [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha), poderá verificar se o arquivo de chave de um componente está presente. No entanto, ainda é possível que outros arquivos pertencentes ao componente estejam ausentes. Nesse cenário, chame [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea). O instalador, em seguida, resolve para qual componente o arquivo pertence e instala o recurso que está vinculado ao componente que requer o menor espaço em disco.

Se a função [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) falhar inesperadamente, você deverá instalar os componentes ausentes.

O procedimento a seguir mostra como instalar componentes ausentes.

**Para detectar e instalar um componente ausente**

1.  Chame [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) para verificar se o arquivo de chave de um componente está presente. No entanto, mesmo que o arquivo de chave do componente esteja presente, ainda é possível que outros arquivos pertencentes ao componente estejam ausentes.
2.  Chame a função [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) se o recurso associado ao componente for desconhecido.
3.  Chame a função [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) ou [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) se o recurso associado ao componente for conhecido.
4.  Chame [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) se um aplicativo não puder abrir um arquivo.

 

 



