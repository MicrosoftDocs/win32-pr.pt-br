---
description: Para instalar assemblies lado a lado como assemblies privados, você pode instalar o assembly como um componente de um pacote do instalador.
ms.assetid: 1cfd836f-a1b9-4339-8756-5488c88b3c2b
title: Instalando assemblies lado a lado como assemblies privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7719a9887f9e92d81e2ad65fe2e75424f0b6957
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748553"
---
# <a name="installing-side-by-side-assemblies-as-private-assemblies"></a>Instalando assemblies lado a lado como assemblies privados

Para instalar [assemblies lado a lado](about-side-by-side-assemblies-.md) como [assemblies privados](/windows/desktop/Msi/private-assemblies), você pode instalar o assembly como um componente de um pacote do instalador. Esse pode ser o mesmo pacote de instalação usado para instalar ou atualizar seu aplicativo. Windows Installer versão 2,0 ou posterior é necessária para instalar assemblies. Para obter mais informações, consulte o SDK do [Windows Installer](../msi/windows-installer-portal.md) e as seções em [instalação de assemblies do Win32](../msi/installation-of-win32-assemblies.md).

Como alternativa, você pode usar o instalador para copiar um assembly privado e um manifesto na mesma pasta que o arquivo executável do aplicativo.

 

 
