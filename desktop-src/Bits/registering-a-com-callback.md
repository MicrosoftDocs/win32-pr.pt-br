---
title: Registrando um retorno de chamada COM
description: Em vez de sondar alterações no status de um trabalho, você pode se registrar para receber notificações quando o status do trabalho for alterado.
ms.assetid: 29350ea4-f7a9-4a42-a531-2cf623fe247b
keywords:
- transferir BITS de trabalho, notificação de eventos
- Registrando para BITS de notificação de eventos
- BITS de notificação de eventos
- BITS de notificação de eventos, retornos de chamada
- BITS de eventos de notificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753feb481a578c30322d18def07418c2dcb611d601fcb438b0e85e843697790b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118680000"
---
# <a name="registering-a-com-callback"></a>Registrando um retorno de chamada COM

Em vez de [sondar](polling-for-the-status-of-the-job.md) alterações no status de um trabalho, você pode se registrar para receber notificações quando o status do trabalho for alterado. Para receber a notificação, você deve implementar a interface [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) . A interface contém os seguintes métodos que o BITS chama, dependendo do seu registro:

-   [**JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred)
-   [**JobError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror)
-   [**JobModification**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)
-   [**Filetransferiu**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred)

Para obter um exemplo que implementa a interface [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) , consulte o código de exemplo no tópico da interface [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .

A interface [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) fornece notificação quando um arquivo é transferido. Normalmente, você usa esse método para validar o arquivo, de modo que o arquivo esteja disponível para os pares baixarem; caso contrário, o arquivo não estará disponível para os pares até que você chame o método [**método ibackgroundcopyjob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) . Para validar o arquivo, chame o método [**IBackgroundCopyFile3:: Setvalidable**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) .

Há dois métodos para registrar um retorno de chamada COM: registrar um objeto de retorno de chamada ou registrar uma ID de classe de retorno de chamada. Usar um objeto de retorno de chamada é mais simples e uma sobrecarga mais baixa; usar um CLSID de retorno de chamada é mais confiável, mas mais complicado. Você pode registrar um, ambos ou nenhum dos BITS usará um objeto de retorno de chamada, se houver, e ainda poderá ser chamado e voltará a criar uma instância de um novo objeto com base em uma ID de classe fornecida se isso falhar.

### <a name="registering-a-callback-object"></a>Registrando um objeto de retorno de chamada

Para registrar sua implementação com o BITS, chame o método [**método ibackgroundcopyjob:: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) . Para especificar quais métodos são chamados por BITS, chame o método [**método ibackgroundcopyjob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags).

A interface de notificação torna-se inválida quando o aplicativo é encerrado; O BITS não mantém a interface de notificação. Como resultado, o processo de inicialização do aplicativo deve registrar os trabalhos existentes para os quais você deseja receber a notificação. Se você precisar capturar informações de estado e de progresso ocorridas desde a última vez em que seu aplicativo foi executado, pesquise informações de estado e progresso durante a inicialização do aplicativo.

Antes de sair, seu aplicativo deve limpar o ponteiro de interface de retorno de chamada (**SetNotifyInterface (NULL)**). É mais eficiente limpar o ponteiro de retorno de chamada do que permitir que o BITS descubra que ele não é mais válido.

Observe que, se mais de um aplicativo chamar o método [**SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) para definir a interface de notificação para o trabalho, o último aplicativo para chamar o método **SetNotifyInterface** é aquele que receberá notificações – os outros aplicativos não receberão notificações.

O exemplo a seguir mostra como registrar-se para notificações. O exemplo supõe que o ponteiro de interface [**método ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) é válido. Para obter detalhes sobre a classe de exemplo CNotifyInterface usada no exemplo a seguir, consulte a interface [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
CNotifyInterface *pNotify = new CNotifyInterface();

if (pNotify)
{
    hr = pJob->SetNotifyInterface(pNotify);
    if (SUCCEEDED(hr))
    {
        hr = pJob->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED | 
                                  BG_NOTIFY_JOB_ERROR );
    }
    pNotify->Release();
    pNotify = NULL;

    if (FAILED(hr))
    {
        //Handle error - unable to register callbacks.
    }
}
```



### <a name="registering-a-callback-clsid"></a>Registrando um CLSID de retorno de chamada

Para registrar um CLSID de retorno de chamada com BITS, chame o método [**IBackgroundCopyJob5:: SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) com a propriedade da **propriedade de trabalho do bits \_ \_ \_ \_ CLSID de notificação** . Para especificar quais métodos são chamados por BITS, chame o método [**método ibackgroundcopyjob:: SetNotifyFlags**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags) .

Você deve garantir que o CLSID de notificação esteja registrado em um servidor COM fora do processo antes de registrar o CLSID com um trabalho do BITS. A implementação de um [servidor com](/windows/desktop/com/com-server-responsibilities) é significativamente mais complicada do que definir e passar um objeto de retorno de chamada, mas oferece várias vantagens importantes. Um servidor COM permite que o BITS mantenha a associação entre um trabalho do BITS e o código do aplicativo entre reinicializações do sistema e para trabalhos grandes ou de longa duração. Um servidor COM também permite que seu aplicativo seja desligado completamente enquanto o BITS continua executando transferências em segundo plano, o que pode melhorar o uso de bateria, CPU e memória do sistema.

Para fornecer uma notificação que você registrou para receber, o BITS primeiro tenta chamar o método correspondente de qualquer objeto de retorno de chamada existente que você possa ter anexado. Se não houver nenhum objeto existente ou se esse objeto existente tiver sido desconectado (normalmente como resultado do encerramento do aplicativo), o BITS chamará CoCreateInstance usando o CLSID de notificação para criar uma instância de um novo objeto de retorno de chamada e usará esse objeto para quaisquer retornos de chamada adicionais até que ele se torne desconectado ou seja substituído por uma nova chamada para [**método ibackgroundcopyjob:: SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface).

Ao contrário dos objetos de retorno de chamada, o CLSID de retorno de chamada será mantido junto com seus trabalhos BITS correspondentes se o serviço BITS ou o sistema forem desligados e reiniciados. Seu aplicativo pode limpar qualquer CLSID de notificação definido anteriormente antes de sair (ou em qualquer outro momento), passando um novo CLSID de notificação de GUID \_ NULL, mas seu aplicativo pode preferir deixar o CLSID de notificação registrado se o seu aplicativo tiver se registrado para fazer com que o com o inicie em resposta a solicitações de CoCreateInstance para seu CLSID. Observe que, se mais de um aplicativo definir o chama a propriedade **CLSID de notificação de \_ Propriedade do trabalho \_ \_ \_ bits** , o último CLSID a ser definido será aquele que o bits usará para instanciar objetos de retorno de chamada – os outros CLSIDs não serão instanciados. Da mesma forma, se um aplicativo registra um CLSID e outro registra um objeto de retorno de chamada, as regras usuais para o objeto de retorno de chamada estão se aplicando e o CLSID não será usado, a menos que o objeto de retorno de chamada seja limpo ou se torne desconectado.

O exemplo a seguir mostra como registrar-se para notificações de CLSID. O exemplo supõe que o ponteiro de interface [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) é válido e que seu aplicativo já foi registrado como um servidor com fora do processo que implementa a classe CNotifyInterface. Para obter detalhes sobre a classe de exemplo CNotifyInterface usada no exemplo a seguir, consulte a interface [**IBackgroundCopyCallback**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback) .


```C++
HRESULT hr; 
IBackgroundCopyJob5* job; 
BITS_JOB_PROPERTY_VALUE propertyValue; 
propertyValue.ClsID = __uuidof(CNotifyInterface); 

hr = job->SetProperty(BITS_JOB_PROPERTY_NOTIFICATION_CLSID, propertyValue); 
if (SUCCEEDED(hr)) 
{ 
    hr = job->SetNotifyFlags(BG_NOTIFY_JOB_TRANSFERRED |  
                             BG_NOTIFY_JOB_ERROR); 
} 

if (FAILED(hr)) 
{ 
    // Handle error - unable to register callbacks. 
} 
```



 

 