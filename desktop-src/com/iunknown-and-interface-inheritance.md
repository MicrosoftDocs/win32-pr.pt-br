---
title: IUnknown e herança de interface
description: IUnknown e herança de interface
ms.assetid: c45f0947-6020-4aa1-9250-561603a46a68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce4d9d164607745b78001bb92b7dc5331296abe
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105788715"
---
# <a name="iunknown-and-interface-inheritance"></a>IUnknown e herança de interface

A herança no COM não significa reutilização de código. Como nenhuma implementação está associada a interfaces, a herança de interface não significa herança de código. Isso significa que apenas o contrato associado a uma interface é herdado de uma classe base pura do C++ e modificado — seja adicionando novos métodos ou qualificando ainda mais o uso permitido de métodos. Não há herança seletiva no COM. Se uma interface herdar de outra, ela incluirá todos os métodos definidos pela outra interface.

A herança é usada COM moderação nas interfaces COM predefinidas. Todas as interfaces predefinidas (e as interfaces personalizadas que você define) herdam suas definições da interface do importante [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), que contém três métodos vitais: [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Todos os objetos COM devem implementar a interface **IUnknown** porque ele fornece os meios, usando **QueryInterface**, para se mover livremente entre as diferentes interfaces que um objeto dá suporte, bem como os meios para gerenciar seu tempo de vida usando **AddRef** e **Release**.

Ao criar um objeto que dá suporte à [agregação](aggregation.md), você precisaria implementar um conjunto de funções [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) para todas as interfaces, bem como uma interface **IUnknown** autônoma. De qualquer forma, qualquer implementador de objeto implementará métodos **IUnknown** . Consulte a seção [usando e implementando IUnknown](using-and-implementing-iunknown.md) para obter mais informações.

Embora existam algumas interfaces que herdam suas definições de uma segunda interface, além de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), a maioria simplesmente herda os métodos de interface **IUnknown** . Isso torna a maioria das interfaces relativamente compactas e fáceis de encapsular.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos e interfaces COM](com-objects-and-interfaces.md)
</dt> </dl>

 

 