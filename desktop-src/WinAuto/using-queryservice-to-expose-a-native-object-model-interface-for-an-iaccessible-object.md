---
title: Usar QueryService para recuperar uma interface nativa para um objeto IAccessible
description: Os desenvolvedores de servidor podem usar essa técnica para expor um ponteiro para um nó de documento personalizado para um objeto IAccessible. Isso pressupõe que você já exponha objetos IAccessible. Essa técnica permite que os clientes obtenham um objeto personalizado de um objeto IAccessible.
ms.assetid: aaa0e840-f8c2-4f3d-9d97-1910f00c1041
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d971462154eb12789a74e8cc6edb5aed68c84b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007844"
---
# <a name="use-queryservice-to-retrieve-a-native-interface-for-an-iaccessible-object"></a>Usar QueryService para recuperar uma interface nativa para um objeto IAccessible

Os desenvolvedores de servidor podem usar essa técnica para expor um ponteiro para um nó de documento personalizado para um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Isso pressupõe que você já exponha objetos **IAccessible** . Essa técnica permite que os clientes obtenham um objeto personalizado de um objeto **IAccessible** .

**Para expor um modelo de objeto nativo para um IAccessible (servidores)**

1.  Adicione suporte para a interface **IServiceProvider** em seu objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .
2.  Defina um GUID que represente a funcionalidade de obter a interface personalizada de um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Isso é chamado de ID de serviço. Você pode usar GUIDGEN.EXE para gerar uma ID de serviço ou reutilizar a ID de interface se tiver uma interface personalizada.
3.  Implemente o método **IServiceProvider:: QueryService** para que ele retorne um ponteiro para a interface personalizada quando chamado com a ID de serviço definida anteriormente neste procedimento. **QueryService** deve retornar **NULL** para todos os outros valores de ID de serviço.
4.  Publique a ID do serviço para que os clientes possam usá-lo.

Os clientes podem usar essa funcionalidade para obter um ponteiro para o objeto personalizado de um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

**Para obter um ponteiro para um objeto personalizado de um IAccessible (clientes)**

1.  Chame [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))(IID \_ IServiceProvider) em um ponteiro de interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para obter um ponteiro de interface **IServiceProvider** .
2.  Chame **IServiceProvider:: QueryService** com a ID de serviço publicada para obter um ponteiro para o objeto personalizado para o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).
3.  Libere a interface **IServiceProvider** se ela não for mais necessária.

Para ser utilizável entre processos, os servidores podem precisar registrar a interface retornada com Component Object Model (COM).

Essa técnica é usada pelo Microsoft Internet Explorer 4,0 e posterior. Ele permite que os clientes obtenham um ponteiro de interface **IHTMLElement2** que corresponde a um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

 

 