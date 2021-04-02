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
# <a name="building-an-iso7816-4-apdu-command"></a><span data-ttu-id="16c80-103">Criando um comando APDU ISO7816-4</span><span class="sxs-lookup"><span data-stu-id="16c80-103">Building an ISO7816-4 APDU Command</span></span>

<span data-ttu-id="16c80-104">Para adicionar funcionalidade a um provedor de serviços, você precisa saber como uma APDU ( [*unidade de dados do protocolo de aplicativo*](/windows/desktop/SecGloss/a-gly) ) ISO7816-4 é criada dentro das DLLs do provedor de serviços base.</span><span class="sxs-lookup"><span data-stu-id="16c80-104">To add functionality to a service provider, you need to know how an ISO7816-4 [*application protocol data unit*](/windows/desktop/SecGloss/a-gly) (APDU) is built within the base service provider DLLs.</span></span> <span data-ttu-id="16c80-105">O procedimento a seguir fornece uma breve visão geral do processo de compilação.</span><span class="sxs-lookup"><span data-stu-id="16c80-105">The following procedure gives a brief overview of the build process.</span></span>

> [!Note]  
> <span data-ttu-id="16c80-106">O exemplo incluído aqui não está necessariamente completo; para obter mais informações, consulte os aplicativos de exemplo e DLLs.</span><span class="sxs-lookup"><span data-stu-id="16c80-106">The example included here is not necessarily complete; for more information, see the sample applications and DLLs.</span></span>

 

<span data-ttu-id="16c80-107">**Para criar um comando ISO7816-4 APDU**</span><span class="sxs-lookup"><span data-stu-id="16c80-107">**To build an ISO7816-4 APDU command**</span></span>

1.  <span data-ttu-id="16c80-108">Crie um objeto [**ISCardCmd**](iscardcmd.md) e um objeto [**ISCardISO7816**](iscardiso7816.md) .</span><span class="sxs-lookup"><span data-stu-id="16c80-108">Create an [**ISCardCmd**](iscardcmd.md) object and an [**ISCardISO7816**](iscardiso7816.md) object.</span></span>

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

    

    <span data-ttu-id="16c80-109">A interface [**ISCardCmd**](iscardcmd.md) contém dois buffers **IByteBuffer** .</span><span class="sxs-lookup"><span data-stu-id="16c80-109">The [**ISCardCmd**](iscardcmd.md) interface contains two **IByteBuffer** buffers.</span></span> <span data-ttu-id="16c80-110">Um buffer contém a cadeia de caracteres de comando APDU real (além de todos os dados a serem enviados com o comando).</span><span class="sxs-lookup"><span data-stu-id="16c80-110">One buffer contains the actual APDU command string (plus any data to send with the command).</span></span> <span data-ttu-id="16c80-111">O outro contém qualquer informação de resposta retornada pelo cartão após a execução do comando.</span><span class="sxs-lookup"><span data-stu-id="16c80-111">The other contains any reply information returned by the card after command execution.</span></span>

2.  <span data-ttu-id="16c80-112">Usando esses objetos, crie um comando ISO7816-4 válido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="16c80-112">Using these objects, create a valid ISO7816-4 command as follows:</span></span>

    ```C++
    //  Do challenge.
    HRESULT hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                             &g_pISCardCmd);
    ```

    

    <span data-ttu-id="16c80-113">Este é o código usado no método [**getchallenge**](iscardiso7816-getchallenge.md) :</span><span class="sxs-lookup"><span data-stu-id="16c80-113">Here is the code used in the [**GetChallenge**](iscardiso7816-getchallenge.md) method:</span></span>

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

    

    <span data-ttu-id="16c80-114">O método [**ISCardISO7816:: getchallenge**](iscardiso7816-getchallenge.md) usa o método [**ISCardCmd:: BuildCmd**](iscardcmd-buildcmd.md) para criar a APDU solicitada.</span><span class="sxs-lookup"><span data-stu-id="16c80-114">The [**ISCardISO7816::GetChallenge**](iscardiso7816-getchallenge.md) method uses the [**ISCardCmd::BuildCmd**](iscardcmd-buildcmd.md) method to build the requested APDU.</span></span> <span data-ttu-id="16c80-115">Isso é feito escrevendo as informações apropriadas no buffer [**ISCardCmd**](iscardcmd.md) APDU na seguinte instrução:</span><span class="sxs-lookup"><span data-stu-id="16c80-115">This is done by writing the appropriate information into the [**ISCardCmd**](iscardcmd.md) APDU buffer in the following statement:</span></span>

    ```C++
    hr = (*ppCmd)->BuildCmd;
    ```

    

3.  <span data-ttu-id="16c80-116">Usando o objeto [**ISCardCmd**](iscardcmd.md) criado, faça uma transação com o cartão, interprete os resultados e continue.</span><span class="sxs-lookup"><span data-stu-id="16c80-116">Using the built [**ISCardCmd**](iscardcmd.md) object, do a transaction with the card, interpret the results, and continue.</span></span>

## <a name="expanding-beyond-iso7816-4"></a><span data-ttu-id="16c80-117">Expandindo além do ISO7816-4</span><span class="sxs-lookup"><span data-stu-id="16c80-117">Expanding Beyond ISO7816-4</span></span>

<span data-ttu-id="16c80-118">A maneira recomendada para expandir o processo de Build/execução do provedor de serviço descrito acima é criar um novo objeto COM.</span><span class="sxs-lookup"><span data-stu-id="16c80-118">The recommended way to expand the service provider build/execute process described above is to create a new COM object.</span></span> <span data-ttu-id="16c80-119">Esse objeto COM deve dar suporte a uma nova interface que permite a criação de comandos não ISO7816-4 e deve agregar a interface [**ISCardISO7816**](iscardiso7816.md) .</span><span class="sxs-lookup"><span data-stu-id="16c80-119">This COM object should support a new interface that allows creation of non-ISO7816-4 commands and should aggregate the [**ISCardISO7816**](iscardiso7816.md) interface.</span></span>

## <a name="example-of-building-an-iso7816-4-apdu-command"></a><span data-ttu-id="16c80-120">Exemplo de criação de um comando APDU ISO7816-4</span><span class="sxs-lookup"><span data-stu-id="16c80-120">Example of Building an ISO7816-4 APDU Command</span></span>

<span data-ttu-id="16c80-121">O exemplo a seguir mostra o código usado no procedimento acima.</span><span class="sxs-lookup"><span data-stu-id="16c80-121">The following example shows the code used in the procedure above.</span></span>


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



 

 
