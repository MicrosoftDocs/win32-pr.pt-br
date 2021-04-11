---
description: Windows Installer é executado como um serviço em computadores usando o Windows de 32 bits ou 64 bits.
ms.assetid: c02fc401-0c9c-49f6-adcc-ed36bdb18fca
title: Sobre Windows Installer em sistemas operacionais de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe9969a3fc1ccd9b63f6bd75b145f9dbc7d8c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/21/2021
ms.locfileid: "104172353"
---
# <a name="about-windows-installer-on-64-bit-operating-systems"></a>Sobre Windows Installer em sistemas operacionais de 64 bits

Windows Installer é executado como um serviço em computadores usando o Windows de 32 bits ou 64 bits. As versões do instalador anteriores à versão 2,0 podem instalar e gerenciar pacotes de Windows Installer de 32 bits somente em sistemas operacionais de 32 bits. Observe que você não pode anunciar ou instalar um aplicativo de 64 bits em um sistema operacional de 32 bits.

Um pacote de Windows Installer deve ser especificado como um pacote de 32 bits ou de 64 bits; Ele não pode ser especificado como neutro. Em um computador que usa um sistema operacional de 64 bits, o serviço de Windows Installer é hospedado em um processo de 64 bits que instala pacotes de 32 bits e de 64 bits. Windows Installer instala três tipos de pacotes do Windows Installer em um computador que executa um sistema operacional de 64 bits:

-   pacotes de 32 bits que contêm apenas componentes de 32 bits.
-   pacotes de 64 bits contendo alguns componentes de 32 bits.
-   pacotes de 64 bits contendo apenas componentes de 64 bits.

As seções a seguir descrevem os dois tipos de pacotes de Windows Installer e as novas propriedades do instalador fornecidas pelo Windows Installer para pacotes de 64 bits.

[Pacotes de Windows Installer de 32 bits](32-bit-windows-installer-packages.md)

[Pacotes de Windows Installer de 64 bits](64-bit-windows-installer-packages.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando pacotes de Windows Installer de 64 bits](using-64-bit-windows-installer-packages.md)
</dt> </dl>

 

 



