---
title: Usando o System-Supplied substituto
description: Usando o System-Supplied substituto
ms.assetid: 6709e5e2-50e0-470f-b618-3d3043f6e180
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444cb94c5564a78ec5580ae8e7f781e91a8a9c15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292809"
---
# <a name="using-the-system-supplied-surrogate"></a>Usando o System-Supplied substituto

Para usar o substituto fornecido pelo sistema para o servidor DLL, registre a DLL especificando uma cadeia de caracteres vazia ou **nula** para o valor [DllSurrogate](dllsurrogate.md) no registro. Quando uma solicitação de ativação para um servidor DLL é criada para o COM, o COM inicia o processo substituto padrão e a DLL solicitada (especificando o CLSID na linha de comando de inicialização internamente) ao mesmo tempo para evitar uma chamada separada. (Para obter informações sobre como executar mais de um servidor DLL em um processo substituto, consulte [compartilhamento substituto](surrogate-sharing.md).)

A implementação padrão do processo substituto é um servidor pseudo COM o estilo de modelo de Threading misto. Quando vários servidores DLL são carregados em um único processo substituto, esse processo garante que cada servidor DLL seja instanciado usando o modelo de threading especificado no registro para esse servidor. Todos os servidores de thread livre carregados residirão juntos no apartamento multi-threaded, enquanto cada servidor Apartment-Threading residirá em um apartamento de thread único. Se um servidor DLL oferecer suporte a ambos os modelos de Threading, o COM escolherá multithreading.

Esse processo substituto é escrito de forma que o COM manipule o descarregamento de servidores DLL e o encerramento do processo substituto.

O substituto fornecido pelo sistema funcionará muito bem para a maioria dos desenvolvedores, bem como muito fácil de usar. No entanto, esses desenvolvedores com considerações especiais podem decidir que um substituto personalizado é necessário. Para obter mais informações, consulte [escrevendo um substituto personalizado](writing-a-custom-surrogate.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Substitutos de DLL](dll-surrogates.md)
</dt> </dl>

 

 




