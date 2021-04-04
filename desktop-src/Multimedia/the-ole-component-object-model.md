---
title: O Component Object Model OLE
description: O Component Object Model OLE
ms.assetid: f3200d81-c2fa-4cc7-bf85-54f6c753a529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 211c41de8c16eb1cabb1e62f475adbbf603e2c92
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "103917775"
---
# <a name="the-ole-component-object-model"></a>O Component Object Model OLE

Os objetos usados pela biblioteca AVIFile fazem parte do Component Object Model OLE. Basicamente, isso significa que eles compartilham determinados métodos que os tornam mais fáceis de trabalhar e os valores que eles retornam são comuns à maioria dos métodos de interface OLE.

O Component Object Model OLE dos manipuladores de arquivo e fluxo usa a interface de **IClassFactory** do OLE para criar instâncias de sua classe de objeto. Como objetos de componente, eles implementam a interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) , que consiste nos métodos [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)), [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)e [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) . A interface **IUnknown** permite que um aplicativo obtenha ponteiros para outras interfaces com suporte no mesmo objeto.

Você pode determinar se um objeto dá suporte a uma interface específica usando o método **QueryInterface** . Se um objeto der suporte a uma interface especificada, **QueryInterface** retornará um ponteiro para essa interface.

Você pode incrementar e decrementar a contagem de referência associada a um objeto usando os métodos [**AddRef**](/previous-versions//dd757100(v=vs.85)) e [**Release**](/previous-versions//dd757102(v=vs.85)) . A contagem de referência permite que vários clientes acessem um objeto. Quando um objeto é usado pelo primeiro aplicativo, sua contagem de referência é definida como 1. Os aplicativos posteriormente usam o método **AddRef** para incrementar a contagem para permitir que o objeto acompanhe o número de vezes que ele é acessado.

Quando um aplicativo é feito usando um objeto, ele chama o método **Release** para diminuir a contagem de referência. Quando a contagem de referência é zero, o objeto não é mais necessário e a **versão** libera todos os recursos que ele usa e destrói o objeto. Como um objeto usa recursos internos transparentes para o aplicativo, o objeto é responsável por liberá-los. Por exemplo, um manipulador de arquivos pode precisar fechar arquivos de disco abertos e liberar memória de buffer quando lançado.

A maioria dos métodos de interface OLE retorna identificadores de resultados que são definidos usando o tipo de dados **HRESULT** . Esse tipo de dados é feito de um código de severidade, informações contextuais, um código de recurso e um código de status. Um identificador de resultado de retorno que indica êxito tem o valor zero. Um valor diferente de zero indica falha e o membro de código de status do identificador de resultado de retorno fornece uma base para interpretação adicional. Para obter informações adicionais sobre identificadores de resultado de retorno de OLE, consulte a *referência do programador de OLE*.

 

 