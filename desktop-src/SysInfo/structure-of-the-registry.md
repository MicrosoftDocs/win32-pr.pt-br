---
description: O Registro é um banco de dados hierárquico que contém dados que são essenciais para a operação do Windows e os aplicativos e serviços executados no Windows.
ms.assetid: 4ed60563-73d8-4134-8cb2-8388734fb18d
title: Estrutura do Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bf104806b5e4e10b4be7387018e714a0db8bf37
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386665"
---
# <a name="structure-of-the-registry"></a>Estrutura do Registro

O Registro é um banco de dados hierárquico que contém dados que são essenciais para a operação do Windows e os aplicativos e serviços executados no Windows. Os dados são estruturados em um formato de árvore. Cada nó na árvore é chamado de *chave*. Cada chave pode conter *subkeys e* entradas de dados chamadas *valores*. Às vezes, a presença de uma chave são todos os dados que um aplicativo requer; outras vezes, um aplicativo abre uma chave e usa os valores associados à chave. Uma chave pode ter qualquer número de valores e os valores podem estar em qualquer formulário. Para obter mais informações, consulte [Tipos de valor do Registro](registry-value-types.md) e Limites de tamanho do elemento do [Registro](registry-element-size-limits.md).

Cada chave tem um nome que consiste em um ou mais caracteres imprimíveis. Os nomes de chave não são sensíveis a minúsculas. Os nomes de chave não podem incluir o caractere de faixa invertida ( \\ ), mas qualquer outro caractere imprimível pode ser usado. Os nomes de valor e os dados podem incluir o caractere de faixa invertida.

O nome de cada sub-chave é exclusivo em relação à chave que está imediatamente acima dela na hierarquia. Os nomes de chave não são localizados em outros idiomas, embora os valores possam ser.

A ilustração a seguir é um exemplo de estrutura de chave do Registro, conforme exibido pelo Editor do Registro.

![janela do editor do Registro](images/regtree.png)

Cada uma das árvores sob **Meu Computador** é uma chave. A **chave HKEY \_ LOCAL \_ MACHINE** tem as seguintes sub-chaves: **HARDWARE,** **SAM,** **SECURITY,** **SOFTWARE** e **SYSTEM.** Cada uma dessas chaves, por sua vez, tem sub-chaves. Por exemplo, a **chave de HARDWARE** tem as sub-chaves **DESCRIPTION,** **DEVICEMAP** e **RESOURCEMAP**; a **chave DEVICEMAP** tem várias sub-chaves, incluindo **VIDEO.**

Cada valor consiste em um nome de valor e seus dados associados, se algum. **MaxObjectNumber** e **VgaCompatible são** valores que contêm dados na sub-chave **VIDEO.**

Uma árvore de Registro pode ter 512 níveis de profundidade. Você pode criar até 32 níveis por vez por meio de uma única chamada à API do Registro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do Registro do Windows](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))
</dt> </dl>

 

 
