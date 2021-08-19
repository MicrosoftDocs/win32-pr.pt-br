---
title: Clientes e servidores COM
description: Um aspecto crítico do COM é como os clientes e servidores interagem.
ms.assetid: 5d1d8613-3087-443d-8547-a767c8ba4959
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d189b464c8e3a32ff378951067275ab29f5fbabc0b2777c2b2226d632a8bfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048654"
---
# <a name="com-clients-and-servers"></a>Clientes e servidores COM

Um aspecto crítico do COM é como os clientes e servidores interagem. Um *cliente com* é qualquer código ou objeto que obtém um ponteiro para um servidor com e usa seus serviços chamando os métodos de suas interfaces. Um *servidor com* é qualquer objeto que forneça serviços aos clientes; esses serviços estão na forma de implementações de interface COM que podem ser chamadas por qualquer cliente capaz de obter um ponteiro para uma das interfaces no objeto de servidor.

Há dois tipos principais de servidores, *em processo* e *fora de processo*. Os servidores em processo são implementados em uma DLL (biblioteca vinculada dinâmica) e os servidores fora do processo são implementados em um arquivo executável (EXE). Os servidores fora do processo podem residir no computador local ou em um computador remoto. Além disso, o COM fornece um mecanismo que permite que um servidor em processo (uma DLL) seja executado em um processo EXE substituto para obter a vantagem de poder executar o processo em um computador remoto. Para obter mais informações, consulte [substitutos de dll](dll-surrogates.md).

Agora, o modelo de programação COM e as construções foram estendidos para que os clientes e servidores COM possam trabalhar juntos na rede, não apenas dentro de um determinado computador. Isso permite que os aplicativos existentes interajam com novos aplicativos e entre si em redes com administração adequada e novos aplicativos possam ser escritos para tirar proveito dos recursos de rede.

Os aplicativos cliente COM não precisam saber como os objetos de servidor são empacotados, se eles são empacotados como objetos em processo (em DLLs) ou como objetos locais ou remotos (em EXEs). O COM distribuído ainda permite que os objetos sejam empacotados como aplicativos de serviço, sincronizando COM com os recursos avançados de integração do sistema e administrativos do Windows.

> [!Note]  
> Ao longo desta documentação, o acrônimo COM é usado em preferência ao DCOM. Isso ocorre porque o DCOM não é separado; é apenas com uma transmissão mais longa. Nos casos em que o que está sendo descrito é especificamente uma operação remota, o termo *com distribuído* é usado.

 

O COM foi projetado para possibilitar a adição do suporte à transparência de local que se estende por uma rede. Ele permite que os aplicativos escritos para computadores únicos sejam executados em uma rede e fornece recursos que estendem esses recursos e que aumentam a segurança necessária em uma rede. (Para obter mais informações, consulte [segurança em com](security-in-com.md).)

COM especifica um mecanismo pelo qual o código de classe pode ser usado por vários aplicativos diferentes.

Para obter mais informações, consulte estes tópicos:

-   [Obtendo um ponteiro para um objeto](getting-a-pointer-to-an-object.md)
-   [Criando um objeto por meio de um objeto de classe](creating-an-object-through-a-class-object.md)
-   [Responsabilidades do servidor COM](com-server-responsibilities.md)
-   [Estado de objeto persistente](persistent-object-state.md)
-   [Fornecendo informações de classe](providing-class-information.md)
-   [Comunicação entre objetos](inter-object-communication.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sincronização de chamadas](call-synchronization.md)
</dt> <dt>

[Segurança em COM](security-in-com.md)
</dt> </dl>

 

 




