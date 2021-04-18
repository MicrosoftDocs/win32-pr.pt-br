---
description: A interface IWbemObjectSink cria uma interface de coletor que pode receber todos os tipos de notificações dentro do modelo de programação WMI.
ms.assetid: 987aea1d-912a-4691-987f-181c1ef1a8a9
ms.tgt_platform: multiple
title: Interface IWbemObjectSink (Wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemObjectSink
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 980865605eadfd5e4cb61a511317dec7838b8e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767710"
---
# <a name="iwbemobjectsink-interface"></a>Interface IWbemObjectSink

A interface **IWbemObjectSink** cria uma interface de coletor que pode receber todos os tipos de notificações dentro do modelo de programação WMI. Os clientes devem implementar essa interface para receber os resultados dos [métodos assíncronos](making-an-asynchronous-call-with-c--.md) de [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)e tipos específicos de notificações de eventos. Os provedores usam, mas não implementam essa interface para fornecer eventos e objetos ao WMI.

Normalmente, os provedores chamam uma implementação fornecida a eles pelo WMI. Nesses casos, chame [**indicar**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) para fornecer objetos ao serviço WMI. Depois disso, chame [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) para indicar o final da sequência de notificação. Você também pode chamar **SetStatus** para indicar erros quando o coletor não tiver nenhum objeto.

Ao programar clientes assíncronos do WMI, o usuário fornece a implementação. O WMI chama os métodos para entregar objetos e definir o status do resultado.

> [!Note]  
> Se um aplicativo cliente passar a mesma interface de coletor em duas chamadas assíncronas sobrepostas diferentes, o WMI não garantirá a ordem do retorno de chamada. Os aplicativos cliente que fazem chamadas assíncronas sobrepostas devem passar objetos de coletor diferentes ou serializar suas chamadas.

 

> [!Note]  
> Como o retorno de chamada para o coletor não pode ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

 

## <a name="members"></a>Membros

A interface **IWbemObjectSink** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWbemObjectSink** tem esses métodos.



| Método                                         | Descrição                                                                                                             |
|:-----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**Indicar**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)   | Recebe objetos de notificação.<br/>                                                                               |
| [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) | Chamado por fontes para indicar o final de uma sequência de notificação ou para enviar outros códigos de status ao coletor.<br/> |



 

## <a name="remarks"></a>Comentários

Ao implementar um coletor de assinatura de evento (**IWbemObjectSink** ou [**IWbemEventSink**](iwbemeventsink.md)), não chame o WMI de dentro dos métodos de [**indicar**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) ou [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) no objeto do coletor. Por exemplo, chamar [**IWbemServices:: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) para cancelar o coletor de dentro de uma implementação de [**indicar**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) pode interferir no estado do WMI. Para cancelar uma assinatura de evento, defina um sinalizador e chame **IWbemServices:: CancelAsyncCall** de outro thread ou objeto. Para implementações que não estão relacionadas a um coletor de eventos, como recuperações de objeto, enum e consulta, você pode chamar de volta para o WMI.

As implementações do coletor devem processar a notificação de eventos dentro de 100 ms porque o thread WMI que entrega a notificação de eventos não pode realizar outro trabalho até que o objeto do coletor tenha concluído o processamento. Se a notificação exigir uma grande quantidade de processamento, o coletor poderá usar uma fila interna para que outro thread manipule o processamento.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir é uma implementação simples de um coletor de objeto. Este exemplo pode ser usado com [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) ou [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) para receber as instâncias retornadas:


```C++
#include <iostream>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")

class QuerySink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone; 

public:
    QuerySink() { m_lRef = 0; }
   ~QuerySink() { bDone = TRUE; }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT STDMETHODCALLTYPE 
        QueryInterface(REFIID riid, void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            /* [in] */
            LONG lObjectCount,
            /* [size_is][in] */
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );
};


ULONG QuerySink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG QuerySink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT QuerySink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT QuerySink::Indicate(long lObjCount, IWbemClassObject **pArray)
{
    for (long i = 0; i < lObjCount; i++)
    {
        IWbemClassObject *pObj = pArray[i];

        // ... use the object.

        // AddRef() is only required if the object will be held after
        // the return to the caller.
    }

    return WBEM_S_NO_ERROR;
}

HRESULT QuerySink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
    printf("QuerySink::SetStatus hResult = 0x%X\n", hResult);
    return WBEM_S_NO_ERROR;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                           |
| parâmetro<br/>                   | <dl> <dt>Wbemcli. h (incluir Wbemidl. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Wbemuuid. lib</dt> </dl>                  |
| DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl>                  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[API COM para WMI](com-api-for-wmi.md)
</dt> <dt>

[Fazendo uma chamada assíncrona com C++](making-an-asynchronous-call-with-c--.md)
</dt> <dt>

[Definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md)
</dt> <dt>

[Recebendo eventos para a duração do seu aplicativo](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

 




