---
title: Fornecendo informações de classe
description: Fornecendo informações de classe
ms.assetid: 808d9a39-4511-4aba-a23f-3c929970503b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a042283ca9ba6eb29bceeacef2c32f9bd401ef09e92eafbc737711d0d930336
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500116"
---
# <a name="providing-class-information"></a>Fornecendo informações de classe

Geralmente, é útil para um cliente de um objeto examinar as informações de tipo do objeto. Considerando o CLSID do objeto, um cliente pode localizar a biblioteca de tipos do objeto usando entradas do Registro e, em seguida, pode verificar a biblioteca de tipos para a entrada de coclasse na biblioteca que corresponde ao CLSID.

No entanto, nem todos os objetos têm um CLSID, embora ainda precisem fornecer informações de tipo. Além disso, é conveniente que um cliente tenha uma maneira de simplesmente pedir a um objeto suas informações de tipo em vez de passar por todo o período para extrair as mesmas informações das entradas do Registro. Essa funcionalidade é importante ao lidar com interfaces de saída em objetos conectáveis. (Consulte [Usando IProvideClassInfo para](using-iprovideclassinfo.md) obter mais informações sobre como os objetos conectáveis fornecem essa funcionalidade.)

Nesses casos, um cliente pode consultar o objeto [**para IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) ou [**IProvideClassInfo2.**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) Se essas interfaces existirem, o cliente chamará o [**método GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) para obter as informações de tipo para a interface.

Ao implementar [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) ou [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2), um objeto especifica que ele pode fornecer informações de tipo para toda a sua classe; ou seja, o que descreveria em sua seção de coclasse de sua biblioteca de tipos, se ela tiver uma. [**GetClassInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iprovideclassinfo-getclassinfo) retorna um **ponteiro ITypeInfo** correspondente às informações de coclasse do objeto. Por meio **desse ponteiro ITypeInfo,** o cliente pode examinar todas as definições de interface de entrada e saída do objeto.

O objeto também pode fornecer [**IProvideClassInfo2.**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) A interface **IProvideClassInfo2** é uma extensão simples para [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) que torna rápido e fácil recuperar identificadores de interface de saída de um objeto para seu conjunto de eventos padrão. **IProvideClassInfo2** é derivado de **IProvideClassInfo.**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Clientes e servidores COM](com-clients-and-servers.md)
</dt> </dl>

 

 




