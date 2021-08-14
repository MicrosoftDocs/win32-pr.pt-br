---
description: Os provedores podem chamar métodos implementados pelo WMI de dentro de suas implementações de método.
ms.assetid: 5bfd9d9b-ffe5-4def-a97d-85c4c01223f0
ms.tgt_platform: multiple
title: Fazendo chamadas para o WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76adae33db786a8174879e6c7e88b62fb69f3c59598ae7f055f41865b32dbf7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317670"
---
# <a name="making-calls-to-wmi"></a>Fazendo chamadas para o WMI

Os provedores podem chamar métodos implementados pelo WMI de dentro de suas implementações de método. No entanto, há considerações especiais quando um provedor chama a implementação de WMI de um método [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) de dentro de sua própria implementação do mesmo método. Essas considerações são importantes, independentemente de o provedor chamar a versão síncrona ou assíncrona do método.

Cada método de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que um provedor pode implementar tem um parâmetro *pCtx* , um ponteiro para uma implementação de interface [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) . Quando o WMI chama o provedor, o WMI passa um ponteiro válido nesse parâmetro. Um provedor sempre deve passar esse mesmo ponteiro em todas as chamadas para o WMI que eles fazem durante a manutenção de solicitações. O inativo para definir *pCtx* adequadamente pode fazer com que o WMI inicie um loop infinito.

O exemplo de código a seguir mostra a maneira correta de chamar a implementação de WMI de [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) de dentro de uma implementação de [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).


```C++
STDMETHODIMP CClassProv::GetObjectAsync (BSTR ObjectPath,
    long lFlags, IWbemContext *pCtx,
    IWbemObjectSink *pHandler)
{
  IWbemClassObject *pclObj = NULL;
  IWbemServices* m_pNamespace;
  HRESULT hr = m_pNamespace->GetObject(
      _bstr_t(L"AClass"), 0, pCtx, &pclObj, 
      NULL );
  pclObj->Release();
  return pHandler->SetStatus(0, hr, NULL, NULL);
}
```



O exemplo de código C++ neste tópico requer as referências a seguir e \# inclui instruções para compilar corretamente.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Os provedores de instância, classe e propriedade não devem emitir nenhuma chamada para o WMI solicitando a modificação de dados durante a manutenção de uma solicitação de leitura. Os únicos provedores que são exceções a essa regra são os provedores de push. Um provedor de Push é um provedor de classe que armazena dados no repositório do WMI e se baseia no WMI para lidar com solicitações de clientes. Durante a manutenção de uma solicitação de leitura, um provedor de push pode atualizar o repositório WMI, mas deve definir o parâmetro *lFlags* para a **atualização do proprietário do \_ sinalizador \_ \_ WBEM** na chamada [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) apropriada.

Os provedores de eventos não devem fazer nenhuma alteração de classe durante a manutenção de uma chamada. Eles também não podem emitir chamadas relacionadas a eventos, como modificar um filtro de eventos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo um provedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protegendo seu provedor](securing-your-provider.md)
</dt> </dl>

 

 



