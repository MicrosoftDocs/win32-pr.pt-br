---
description: O registro é um banco de dados hierárquico que contém o que é essencial para a operação do Windows e os aplicativos e serviços que são executados no Windows.
ms.assetid: 4ed60563-73d8-4134-8cb2-8388734fb18d
title: Estrutura do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b76b7f827ae3ea96d75d089c7d874c3d31d030
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104550833"
---
# <a name="structure-of-the-registry"></a>Estrutura do registro

O registro é um banco de dados hierárquico que contém o que é essencial para a operação do Windows e os aplicativos e serviços que são executados no Windows. Os dados são estruturados em um formato de árvore. Cada nó na árvore é chamado de *chave*. Cada chave pode conter *subchaves* e entradas de dados chamadas *valores*. Às vezes, a presença de uma chave é todos os dados que um aplicativo requer; em outras ocasiões, um aplicativo abre uma chave e usa os valores associados à chave. Uma chave pode ter qualquer número de valores, e os valores podem estar em qualquer formato. Para obter mais informações, consulte [tipos de valor do registro](registry-value-types.md) e [limites de tamanho do elemento do registro](registry-element-size-limits.md).

Cada chave tem um nome que consiste em um ou mais caracteres imprimíveis. Os nomes de chave não diferenciam maiúsculas de minúsculas. Os nomes de chave não podem incluir o caractere de barra invertida ( \) , mas qualquer outro caractere imprimível pode ser usado. Os nomes de valor e os dados podem incluir o caractere de barra invertida.

O nome de cada subchave é exclusivo em relação à chave que está imediatamente acima dela na hierarquia. Os nomes de chave não são localizados em outras linguagens, embora os valores possam ser.

A ilustração a seguir é um exemplo de estrutura de chave do registro, conforme exibido pelo editor do registro.

![janela do editor do registro](images/regtree.png)

Cada uma das árvores em **meu computador** é uma chave. A chave do **\_ \_ computador local hKey** tem as seguintes subchaves: **hardware**, **Sam**, **Security**, **software** e **System**. Cada uma dessas chaves, por sua vez, tem subchaves. Por exemplo, a chave de **hardware** tem as subchaves **Description**, **DEVICEMAP** e **RESOURCEMAP**; a chave **DEVICEMAP** tem várias subchaves, incluindo **vídeo**.

Cada valor consiste em um nome de valor e seus dados associados, se houver. **MaxObjectNumber** e **VgaCompatible** são valores que contêm dados sob a subchave **Video** .

Uma árvore do registro pode ter 512 níveis de profundidade. Você pode criar até 32 níveis por vez por meio de uma única chamada à API do registro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do registro do Windows](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))
</dt> </dl>

 

 
