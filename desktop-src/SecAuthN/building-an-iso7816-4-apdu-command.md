---
description: O procedimento a seguir fornece uma breve visão geral do processo de compilação.
ms.assetid: a369d4d7-bd4b-4b4d-846e-ad85251e9ffb
title: Criando um comando APDU ISO7816-4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63987f27e74dd30b4520e6e09f27ae716d793d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164869"
---
# <a name="building-an-iso7816-4-apdu-command"></a>Criando um comando APDU ISO7816-4

Para adicionar funcionalidade a um provedor de serviços, você precisa saber como uma APDU ( [*unidade de dados do protocolo de aplicativo*](/windows/desktop/SecGloss/a-gly) ) ISO7816-4 é criada dentro das DLLs do provedor de serviços base. O procedimento a seguir fornece uma breve visão geral do processo de compilação.

> [!Note]  
> O exemplo incluído aqui não está necessariamente completo; para obter mais informações, consulte os aplicativos de exemplo e DLLs.

 

**Para criar um comando ISO7816-4 APDU**

1.  Crie um objeto [**ISCardCmd**](iscardcmd.md) e um objeto [**ISCardISO7816**](iscardiso7816.md) .

    ```C++
    //  Create an ISCardCmd object.
    HRESULT hresult = CoCreateInstance(CLSID_CSCardCmd,
                               NULL,
                               CLSCTX_ALL,
                               IID_ISCardCmd,
                               (LPVOID*) &g_pISCardCmd);
    //  Create an ISCardISO7816 object.
    HRESULT hresult = CoCreateInstance(CLSID_CSCardISO7816,
                               NULL,
                               CLSCTX_ALL,
                               IID_ISCardISO7816,
                               (LPVOID*) &g_pISCardISO7816);
    ```

    

    A interface [**ISCardCmd**](iscardcmd.md) contém dois buffers **IByteBuffer** . Um buffer contém a cadeia de caracteres de comando APDU real (além de todos os dados a serem enviados com o comando). O outro contém qualquer informação de resposta retornada pelo cartão após a execução do comando.

2.  Usando esses objetos, crie um comando ISO7816-4 válido da seguinte maneira:

    ```C++
    //  Do challenge.
    HRESULT hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                             &g_pISCardCmd);
    ```

    

    Este é o código usado no método [**getchallenge**](iscardiso7816-getchallenge.md) :

    ```C++
    #include <windows.h>

    STDMETHODIMP CSCardISO7816::GetChallenge(IN DWORD dwBytesExpected /*= 0*/,
                                IN OUT LPSCARDCMD *ppCmd)
    {
        //  Locals.
        HRESULT hr = S_OK;
        
        try
        {
            //  Is the ISCardCmd object okay?
            hr = IsSCardCmdValid(ppCmd);
            if (FAILED(hr))
                throw (hr);

            //  Do it.
            hr = (*ppCmd)->BuildCmd(m_byClassId,
                                    (BYTE) INS_GET_CHALLENGE,
                                    (BYTE) INS_NULL,  // P1 = 0x00
                                    (BYTE) INS_NULL,  // P2 = 0x00
                                    NULL,
                                    &dwBytesExpected);
            if (FAILED(hr))
                throw (hr);
        }
    }
    ```

    

    O método [**ISCardISO7816:: getchallenge**](iscardiso7816-getchallenge.md) usa o método [**ISCardCmd:: BuildCmd**](iscardcmd-buildcmd.md) para criar a APDU solicitada. Isso é feito escrevendo as informações apropriadas no buffer [**ISCardCmd**](iscardcmd.md) APDU na seguinte instrução:

    ```C++
    hr = (*ppCmd)->BuildCmd;
    ```

    

3.  Usando o objeto [**ISCardCmd**](iscardcmd.md) criado, faça uma transação com o cartão, interprete os resultados e continue.

## <a name="expanding-beyond-iso7816-4"></a>Expandindo além do ISO7816-4

A maneira recomendada para expandir o processo de Build/execução do provedor de serviço descrito acima é criar um novo objeto COM. Esse objeto COM deve dar suporte a uma nova interface que permite a criação de comandos não ISO7816-4 e deve agregar a interface [**ISCardISO7816**](iscardiso7816.md) .

## <a name="example-of-building-an-iso7816-4-apdu-command"></a>Exemplo de criação de um comando APDU ISO7816-4

O exemplo a seguir mostra o código usado no procedimento acima.


```C++
//  Create an ISCardCmd object.
hresult = CoCreateInstance(CLSID_CSCardCmd,
                           NULL,
                           CLSCTX_ALL,
                           IID_ISCardCmd,
                           (LPVOID*) &g_pISCardCmd);
//  Create an ISCardISO7816 object.
hresult = CoCreateInstance(CLSID_CSCardISO7816,
                           NULL,
                           CLSCTX_ALL,
                           IID_ISCardISO7816,
                           (LPVOID*) &g_pISCardISO7816);
//  Do challenge.
hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                         &g_pISCardCmd);

STDMETHODIMP
CSCardISO7816::GetChallenge(IN DWORD dwBytesExpected /*= 0*/,
                            IN OUT LPSCARDCMD *ppCmd)
{
    //  Locals.
    HRESULT hr = S_OK;
    
    try
    {
        //  Is the ISCardCmd object okay?
        hr = IsSCardCmdValid(ppCmd);
        if (FAILED(hr))
            throw (hr);

        //  Do it.
        hr = (*ppCmd)->BuildCmd(m_byClassId,
                                (BYTE) INS_GET_CHALLENGE,
                                (BYTE) INS_NULL,  // P1 = 0x00
                                (BYTE) INS_NULL,  // P2 = 0x00
                                NULL,
                                &dwBytesExpected);
        if (FAILED(hr))
            throw (hr);
    }
}
```



 

 
