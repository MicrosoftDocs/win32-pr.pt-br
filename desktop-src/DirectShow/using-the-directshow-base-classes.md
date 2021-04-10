---
description: Usando as classes base do DirectShow
ms.assetid: 7eab0e55-1566-4b4c-b37c-32c5a1f37363
title: Usando as classes base do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 870c910505d6df42d0b9a6094470bf803b83d6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170271"
---
# <a name="using-the-directshow-base-classes"></a>Usando as classes base do DirectShow

Para usar as classes base no DirectShow, você deve criar e vincular a biblioteca de classes base.

A biblioteca de classes base é fornecida como um exemplo de SDK no Microsoft Windows Software Development Kit (SDK) ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ). O local exato depende da versão do SDK que você instalou, mas o caminho relativo é:

*(Raiz de exemplos do SDK)* \\ BaseClasses do DirectShow \\

Cabeçalho: Streams. h

Biblioteca: o exemplo compila versões de varejo e de depuração da biblioteca:

-   Versão de varejo: Strmbase. lib
-   Versão de depuração: Strmbasd. lib.

Para obter mais informações sobre como configurar o ambiente de compilação, consulte [Configurando o ambiente de compilação](setting-up-the-build-environment.md).

## <a name="preprocessor-symbols"></a>Símbolos de pré-processador

Quando você inclui o arquivo de cabeçalho Streams. h, os seguintes símbolos de pré-processador têm um significado especial:

-   PERF: reservado. Não use este símbolo de pré-processador.
-   VFWROBUST: habilita a validação de ponteiro no varejo. Para obter mais informações, consulte [macros de validação de ponteiro](pointer-validation-macros.md). Em compilações de depuração, não é necessário definir VFWROBUST.

> [!Note]  
> No Windows Vista e posterior, as macros de validação do ponteiro estão vazias.

 

 

 



