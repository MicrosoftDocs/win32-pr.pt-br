---
description: Msitool. Mak é um makefile que você pode usar para criar ferramentas e ações personalizadas.
ms.assetid: c05da933-7e0e-4fbb-a936-517902a363c4
title: Msitool. Mak
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3dad9fd65aaa880e9fdb38369843907104dea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091450"
---
# <a name="msitoolmak"></a>Msitool. Mak

Msitool. Mak é um makefile que você pode usar para criar ferramentas e ações personalizadas. Ele pode ser usado com Visual C++ versão 4,0 ou posterior. Para obter mais informações, consulte o arquivo de cabeçalho. Ele requer um conjunto de valores a serem definidos antes de incluir esse arquivo. Normalmente, os desenvolvedores colocam esses no início do. cpp, ifdef deve ser ignorado pelo compilador do C. Da mesma forma, os recursos são adicionados ao final do arquivo. cpp. Consulte os exemplos para obter detalhes.

VCBIN pode ser definido para o diretório onde as ferramentas de Visual C++ são encontradas ou o makefile usa MSVCDIR e MSDEVDIR. Se eles não estiverem definidos, ele não especificará um local, supondo que as ferramentas estejam no caminho. Um problema com as variáveis de ambiente no Visual C++ versão 5,0 é que, se ambos não estiverem no caminho, o vinculador não poderá encontrar Msdis100.dll. Se você copiá-lo de MSDEVDIR para MSVCDIR, ele funcionará. A outra opção é copiar Msdis100.dll e Rc.exe e Rcdll.dll para MSVCDIR e definir VCBIN para isso.

Essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ferramentas de desenvolvimento Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Versões, ferramentas e redistribuíveis liberados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



