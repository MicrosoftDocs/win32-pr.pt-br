---
title: O OLE Component Object Model
description: O OLE Component Object Model
ms.assetid: f3200d81-c2fa-4cc7-bf85-54f6c753a529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5de83641250c912efbe92d7181deb52b477af06e2b49598ee63762488a932687
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805016"
---
# <a name="the-ole-component-object-model"></a>O OLE Component Object Model

Os objetos usados pela biblioteca AVIFile fazem parte da biblioteca OLE Component Object Model. Basicamente, isso significa que eles compartilham determinados métodos que os facilitam o trabalho, e os valores que retornam são comuns à maioria dos métodos de interface OLE.

A Component Object Model OLE dos manipuladores de arquivo e fluxo usa a interface OLE **IClassFactory** para criar instâncias de sua classe de objeto. Como objetos de componente, eles implementam a interface [IUnknown,](/windows/win32/api/unknwn/nn-unknwn-iunknown) que consiste nos métodos [**QueryInterface,**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)) [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)e [**AddRef.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) A **interface IUnknown** permite que um aplicativo obtenha ponteiros para outras interfaces com suporte pelo mesmo objeto.

Você pode determinar se um objeto dá suporte a uma interface específica usando **o método QueryInterface.** Se um objeto dá suporte a uma interface especificada, **QueryInterface** retorna um ponteiro para essa interface.

Você pode incrementar e decrementar a contagem de referência associada a um objeto usando os [**métodos AddRef**](/previous-versions//dd757100(v=vs.85)) e [**Release.**](/previous-versions//dd757102(v=vs.85)) A contagem de referência permite que vários clientes acessem um objeto . Quando um objeto é usado pelo primeiro aplicativo, sua contagem de referência é definida como 1. Os aplicativos posteriormente usam **o método AddRef** para incrementar a contagem para permitir que o objeto acompanhe o número de vezes que ele é acessado.

Quando um aplicativo é feito usando um objeto , ele chama o **método Release** para decrementar a contagem de referência. Quando a contagem de referência é zero,  o objeto não é mais necessário e Release libera todos os recursos que ele usa e destrói o objeto. Como um objeto usa recursos internos transparentes para o aplicativo, o objeto é responsável por libera-los. Por exemplo, um manipulador de arquivos pode precisar fechar arquivos de disco abertos e liberar memória de buffer quando liberado.

A maioria dos métodos de interface OLE retorna identificadores de resultado definidos usando o tipo **de dados HRESULT.** Esse tipo de dados é feito de um código de severidade, informações contextuais, um código de instalação e um código de status. Um alça de resultado de retorno que indica êxito tem o valor zero. Um valor diferente de zero indica falha e o membro do código de status do alça de resultado de retorno fornece uma base para interpretação adicional. Para obter informações adicionais sobre as alças de resultado de retorno OLE, consulte Referência *do programador OLE*.

 

 