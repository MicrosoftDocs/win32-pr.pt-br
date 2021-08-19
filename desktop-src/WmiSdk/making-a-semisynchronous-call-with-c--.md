---
description: 'Chamadas Semisynchronous são os meios recomendados para chamar métodos WMI, como os métodos IWbemServices:: ExecMethod e Provider, como o método chkdsk da classe do disco \_ lógico do Win32.'
ms.assetid: 3d5ddd77-19f7-42d0-b8ca-a0a11f6b3f0f
ms.tgt_platform: multiple
title: Fazendo uma chamada Semisynchronous com C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a550c5ad659ab9b640a1fcb3060b5f6cc7671f80c209d238cd859ad0ef6f49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050694"
---
# <a name="making-a-semisynchronous-call-with-c"></a>Fazendo uma chamada Semisynchronous com C++

Chamadas Semisynchronous são os meios recomendados para chamar métodos WMI, como os métodos [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) e Provider, como o [**método chkdsk da classe do disco \_ lógico do Win32**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk).

Uma desvantagem do processamento síncrono é que o thread do chamador é bloqueado até que a chamada seja concluída. O bloqueio pode causar um atraso no tempo de processamento. Por outro lado, uma chamada assíncrona deve implementar [**SWbemSink**](swbemsink.md) no script. Em C++, o código assíncrono deve implementar a interface [**IWbemObjectSink**](iwbemobjectsink.md) , usar vários threads e controlar o fluxo de informações de volta para o chamador. Conjuntos de resultados grandes de consultas, por exemplo, podem levar um tempo considerável para fornecer e obriga o chamador a gastar recursos de sistema significativos para lidar com a entrega.

O processamento de Semisynchronous resolve o bloqueio de thread e os problemas de entrega não controlados sondando um objeto de status especial que implementa a interface [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) . Por meio do **IWbemCallResult**, você pode melhorar a velocidade e a eficiência de consultas, enumerações e notificações de eventos.

O procedimento a seguir descreve como fazer uma chamada semisynchronous com a interface [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

**Para fazer uma chamada semisynchronous com a interface IWbemServices**

1.  Faça sua chamada normalmente, mas com o **sinalizador WBEM \_ , \_ retorne \_ imediatamente** o sinalizador definido no parâmetro *iFlags* .

    Você pode combinar **o \_ retorno do sinalizador WBEM \_ \_ imediatamente** com outros sinalizadores que são válidos para o método específico. Por exemplo, use o sinalizador de **\_ \_ \_ somente encaminhamento do sinalizador WBEM** para todas as chamadas que retornam enumeradores. Definir esses sinalizadores em combinação economiza tempo e espaço e melhora a capacidade de resposta.

2.  Sondar seus resultados.

    Se você chamar um método que retorna um enumerador, como [**IWbemServices:: CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) ou [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), poderá sondar os enumeradores com os métodos [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) ou [**IEnumWbemClassObject:: NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) . A chamada **IEnumWbemClassObject:: NextAsync** é não bloqueada e retorna imediatamente. Em segundo plano, o WMI começa a entregar o número solicitado de objetos chamando [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate). Em seguida, o WMI para e aguarda outra chamada **NextAsync** .

    Se você chamar um método que não retorna um enumerador, como [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), deverá definir o parâmetro *ppCallResult* como um ponteiro válido. Use o [**IWbemCallResult:: GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) no ponteiro retornado para recuperar o **WBEM \_ S \_ sem \_ erro**.

3.  Conclua sua chamada.

    Para uma chamada que retorna um enumerador, o WMI chama [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) para relatar a conclusão da operação. Se você não precisar do resultado inteiro, libere o enumerador chamando o método [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) . Chamar resultados de **liberação** no WMI cancela a entrega de todos os objetos que permanecem.

    Para uma chamada que não usa um enumerador, recupere o objeto [**GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) por meio do parâmetro *plStatus* do seu método.

O exemplo de código C++ neste tópico requer as seguintes \# instruções include para serem compiladas corretamente.


```C++
#include <comdef.h>
#include <wbemidl.h>
```



O exemplo de código a seguir mostra como fazer uma chamada de semisynchronous para [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).


```C++
void GetObjSemiSync(IWbemServices *pSvc)
{

    IWbemCallResult *pCallRes = 0;
    IWbemClassObject *pObj = 0;
    
    HRESULT hRes = pSvc->GetObject(_bstr_t(L"MyClass=\"AAA\""), 0,
        0, 0, &pCallRes
        );
        
    if (hRes || pCallRes == 0)
        return;
        
    while (true)
    {
        LONG lStatus = 0;
        HRESULT hRes = pCallRes->GetCallStatus(5000, &lStatus);
        if ( hRes == WBEM_S_NO_ERROR || hRes != WBEM_S_TIMEDOUT )
            break;

        // Do another task
    }

    hRes = pCallRes->GetResultObject(5000, &pObj);
    if (hRes)
    {
        pCallRes->Release();
        return;
    }

    pCallRes->Release();

    // Use the object.

    // ...

    // Release it.
    // ===========
        
    pObj->Release();    // Release objects not owned.            
  
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chamando um método](calling-a-method.md)
</dt> </dl>

 

 
