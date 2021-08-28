---
description: Windows O instalador é executado como um serviço em computadores que usam 32 bits ou 64 bits Windows.
ms.assetid: c02fc401-0c9c-49f6-adcc-ed36bdb18fca
title: Sobre Windows instalador em sistemas operacionais de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a6ad9356fe854cc35799dbe14766ae67a9e0f0b947230914a31e436f4bc7cf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119382966"
---
# <a name="about-windows-installer-on-64-bit-operating-systems"></a>Sobre Windows instalador em sistemas operacionais de 64 bits

Windows O instalador é executado como um serviço em computadores que usam 32 bits ou 64 bits Windows. Versões do instalador anteriores à versão 2.0 podem instalar e gerenciar pacotes do instalador de 32 bits Windows somente em sistemas operacionais de 32 bits. Observe que você não pode anunciar ou instalar um aplicativo de 64 bits em um sistema operacional de 32 bits.

Um Windows instalador deve ser especificado como um pacote de 32 bits ou de 64 bits; ele não pode ser especificado como neutro. Em um computador que usa um sistema operacional de 64 bits, o serviço instalador do Windows é hospedado em um processo de 64 bits que instala pacotes de 32 e 64 bits. Windows O instalador instala três tipos de pacotes Windows instalador em um computador que executa um sistema operacional de 64 bits:

-   Pacotes de 32 bits que contêm apenas componentes de 32 bits.
-   Pacotes de 64 bits que contêm alguns componentes de 32 bits.
-   Pacotes de 64 bits que contêm apenas componentes de 64 bits.

As seções a seguir descrevem os dois tipos de pacotes do instalador Windows e as novas propriedades do instalador fornecidas pelo instalador Windows para pacotes de 64 bits.

[Pacotes do instalador Windows de 32 bits](32-bit-windows-installer-packages.md)

[Pacotes do instalador Windows 64 bits](64-bit-windows-installer-packages.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando pacotes do instalador Windows 64 bits](using-64-bit-windows-installer-packages.md)
</dt> </dl>

 

 



