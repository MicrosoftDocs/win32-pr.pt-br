---
description: Um assembly Win32 pode ser instalado como um assembly privado e estar exclusivamente disponível para uso por um aplicativo. Os assemblies privados devem ser instalados por um pacote Windows Installer usado para instalar ou atualizar um aplicativo.
ms.assetid: 4c6dac5f-fdd3-4125-b54a-74941ee6b3b4
title: Assemblies particulares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1073426e080cc4b8b30358ce26feb99515abb185
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169844"
---
# <a name="private-assemblies"></a>Assemblies particulares

Um assembly Win32 pode ser instalado como um assembly privado e estar exclusivamente disponível para uso por um aplicativo. Os assemblies privados devem ser instalados por um pacote Windows Installer usado para instalar ou atualizar um aplicativo.

No Windows XP, os assemblies privados são instalados como [assemblies lado a lado](side-by-side-assemblies.md). O Windows Installer instala assemblies privados lado a lado em uma pasta privada para o aplicativo. Normalmente, a pasta que contém o arquivo executável dos aplicativos. A dependência do aplicativo no assembly particular é especificada em um arquivo de manifesto do aplicativo. Para obter mais informações, consulte [aplicativos isolados e assemblies lado a lado](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md).

Em sistemas operacionais anteriores ao Windows XP, uma cópia do assembly particular e um arquivo. local são instalados em uma pasta particular para o uso exclusivo do aplicativo. Uma versão do assembly também é registrada globalmente no sistema e disponível para qualquer aplicativo que se vincule a ele. A versão global do assembly pode ser a versão instalada com o aplicativo ou uma versão anterior. A versão global é determinada pelas mesmas regras usadas por [componentes isolados](isolated-components.md).

Observe que o Windows Installer não pode instalar um assembly privado em um local que tenha um caminho que contenha mais de 234 caracteres, incluindo o caractere nulo de terminação.

 

 
