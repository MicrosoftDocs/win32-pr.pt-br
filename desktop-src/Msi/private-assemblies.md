---
description: Um assembly Win32 pode ser instalado como um assembly privado e estar disponível exclusivamente para uso por um aplicativo. Os assemblies privados devem ser instalados por um Windows instalador de dados usado para instalar ou atualizar um aplicativo.
ms.assetid: 4c6dac5f-fdd3-4125-b54a-74941ee6b3b4
title: Assemblies particulares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45cc9bd9c9f4c5230dcb24ed7059f6817d4c5f3c7cfdeb4b7cfd25d95ca2a3eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327837"
---
# <a name="private-assemblies"></a>Assemblies particulares

Um assembly Win32 pode ser instalado como um assembly privado e estar disponível exclusivamente para uso por um aplicativo. Os assemblies privados devem ser instalados por um Windows instalador de dados usado para instalar ou atualizar um aplicativo.

No Windows XP, os assemblies privados são instalados como [assemblies lado a lado.](side-by-side-assemblies.md) O Windows instala assemblies particulares lado a lado em uma pasta privada para o aplicativo. Normalmente, a pasta que contém o arquivo executável de aplicativos. A dependência do aplicativo no assembly privado é especificada em um arquivo de manifesto do aplicativo. Para obter mais informações, [consulte Aplicativos isolados e Assemblies lado a lado.](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)

Em sistemas operacionais anteriores Windows XP, uma cópia do assembly privado e um arquivo .local é instalada em uma pasta privada para uso exclusivo do aplicativo. Uma versão do assembly também é registrada globalmente no sistema e está disponível para qualquer aplicativo que se a bind a ele. A versão global do assembly pode ser a versão instalada com o aplicativo ou uma versão anterior. A versão global é determinada pelas mesmas regras usadas pelos [Componentes Isolados.](isolated-components.md)

Observe que o Windows instalador não pode instalar um assembly privado em um local com um caminho que contenha mais de 234 caracteres, incluindo o caractere nulo de terminação.

 

 
