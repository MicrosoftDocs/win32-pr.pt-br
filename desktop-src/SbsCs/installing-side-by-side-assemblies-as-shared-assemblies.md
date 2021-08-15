---
description: O procedimento a seguir descreve como instalar assemblies lado a lado como assemblies compartilhados.
ms.assetid: 272ad1b8-9ea2-4af8-ba0d-c59f4db027e6
title: Instalando assemblies lado a lado como assemblies compartilhados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6348354b224e281135e72697aaa155ce69f4ccd23293f671d733e2bc1cd89dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127506"
---
# <a name="installing-side-by-side-assemblies-as-shared-assemblies"></a>Instalando assemblies lado a lado como assemblies compartilhados

O procedimento a seguir descreve como instalar [assemblies lado a lado](about-side-by-side-assemblies-.md) como [assemblies compartilhados](/windows/desktop/Msi/shared-assemblies).

**Para instalar um assembly lado a lado como um assembly compartilhado**

1.  Assine e crie um catálogo para os arquivos no assembly.

    Os arquivos devem ser assinados para instalá-los como assemblies lado a lado. Para obter mais informações, consulte [criando arquivos e catálogos assinados](creating-signed-files-and-catalogs.md).

2.  você deve instalar assemblies compartilhados lado a lado como componentes de um pacote de Windows Installer. Esse pode ser o mesmo pacote de instalação usado para instalar ou atualizar seu aplicativo. Se o assembly compartilhado for enviado como parte de vários aplicativos, você deverá fornecer um módulo de mesclagem que possa ser incorporado nos pacotes de instalação desses aplicativos e criar um catálogo para os arquivos no assembly.

    Windows O instalador versão 2,0 ou posterior é necessário para instalar assemblies. para obter mais informações, consulte o SDK do [Windows Installer](../msi/windows-installer-portal.md) e as seções em [instalação de Assemblies do Win32](../msi/installation-of-win32-assemblies.md).

 

 
