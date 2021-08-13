---
title: Registrando um retorno de chamada COM
description: Em vez de sondar alterações no status de um trabalho, você pode registrar-se para receber a notificação quando o status do trabalho mudar.
ms.assetid: 29350ea4-f7a9-4a42-a531-2cf623fe247b
keywords:
- transferir bits de trabalho , notificação de eventos
- registrando para BITS de notificação de eventos
- BITS de notificação de eventos
- bits de notificação de eventos, retornos de chamada
- bits de eventos de notificação
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

Em vez [de sondar](polling-for-the-status-of-the-job.md) alterações no status de um trabalho, você pode registrar-se para receber a notificação quando o status do trabalho mudar. Para receber a notificação, você deve implementar a interface [**IBackgroundCopyCallback2.**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) A interface contém os seguintes métodos que o BITS chama, dependendo do registro:

-   [**JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred)
-   [**JobError**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-joberror)
-   [**JobModification**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobmodification)
-   [**FileTransferred**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopycallback2-filetransferred)

Para ver um exemplo que implementa a interface [**IBackgroundCopyCallback2,**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) consulte o código de exemplo no tópico interface [**IBackgroundCopyCallback.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback)

A interface [**IBackgroundCopyCallback2**](/windows/desktop/api/Bits3_0/nn-bits3_0-ibackgroundcopycallback2) fornece notificação quando um arquivo é transferido. Normalmente, você usa esse método para validar o arquivo, de modo que o arquivo está disponível para os pares baixarem; caso contrário, o arquivo não estará disponível para pares até que você chame o [**método IBackgroundCopyJob::Complete.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) Para validar o arquivo, chame [**o método IBackgroundCopyFile3::SetValidationState.**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate)

Há dois métodos para registrar um retorno de chamada COM: registrar um objeto de retorno de chamada ou registrar uma ID de classe de retorno de chamada. Usar um objeto de retorno de chamada é uma sobrecarga mais simples e mais baixa; usar um CLSID de retorno de chamada é mais confiável, mas mais complicado. Você pode registrar um, ambos ou nenhum – o BITS usará um objeto de retorno de chamada se um existir e ainda puder ser chamado e fará fallback para a inciação de um novo objeto com base em uma ID de classe fornecida, se isso falhar.

### <a name="registering-a-callback-object"></a>Registrando um objeto de retorno de chamada

Para registrar sua implementação com BITS, chame o [**método IBackgroundCopyJob::SetNotifyInterface.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) Para especificar quais métodos o BITS chama, chame [**o método IBackgroundCopyJob::SetNotifyFlags.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)

A interface de notificação se torna inválida quando o aplicativo é encerrado; BITS não persiste a interface de notificação. Como resultado, o processo de inicialização do aplicativo deve registrar trabalhos existentes para os quais você deseja receber a notificação. Se você precisar capturar informações de estado e progresso que ocorreram desde a última vez que seu aplicativo foi executado, sondar informações de estado e progresso durante a inicialização do aplicativo.

Antes de sair, seu aplicativo deve limpar o ponteiro da interface de retorno de chamada (**SetNotifyInterface(NULL)**). É mais eficiente limpar o ponteiro de retorno de chamada do que permitir que o BITS descubra que ele não é mais válido.

Observe que, se mais de um aplicativo chamar o método [**SetNotifyInterface**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface) para definir a interface de notificação para o trabalho, o último aplicativo a chamar o método **SetNotifyInterface** será aquele que receberá notificações – os outros aplicativos não receberão notificações.

O exemplo a seguir mostra como se registrar para notificações. O exemplo pressupo que o ponteiro da interface [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) é válido. Para obter detalhes sobre a classe de exemplo CNotifyInterface usada no exemplo a seguir, consulte a interface [**IBackgroundCopyCallback.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback)


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

Para registrar um CLSID de retorno de chamada com BITS, chame o método [**IBackgroundCopyJob5::SetProperty**](/windows/desktop/api/Bits5_0/nf-bits5_0-ibackgroundcopyjob5-setproperty) com a **PROPERTY NOTIFICATION \_ \_ \_ \_ CLSID** propertyId do BITS JOB. Para especificar quais métodos o BITS chama, chame [**o método IBackgroundCopyJob::SetNotifyFlags.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyflags)

Você deve garantir que a CLSID de notificação esteja registrada em um servidor COM fora do processo antes de registrar o CLSID com um trabalho bits. Implementar um [servidor COM é significativamente](/windows/desktop/com/com-server-responsibilities) mais complicado do que definir e passar um objeto de retorno de chamada, mas oferece várias vantagens importantes. Um servidor COM permite que o BITS mantenha a associação entre um trabalho BITS e o código do aplicativo entre reinicializações do sistema e para trabalhos grandes ou de longa duração. Um servidor COM também permite que seu aplicativo seja desligado completamente enquanto o BITS continua executando transferências em segundo plano, o que pode melhorar o uso de bateria, CPU e memória do sistema.

Para fornecer uma notificação que você registrou para receber, o BITS primeiro tenta chamar o método correspondente de qualquer objeto de retorno de chamada existente que você possa ter anexado. Se não houver nenhum objeto existente ou se esse objeto existente tiver se desconectado (normalmente como resultado do encerramento do aplicativo), o BITS chamará CoCreateInstance usando a CLSID de notificação para insinciar um novo objeto de retorno de chamada e usará esse objeto para quaisquer retornos de chamada posteriores até que ele seja desconectado ou substituído por uma nova chamada para [**IBackgroundCopyJob::SetNotifyInterface.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setnotifyinterface)

Ao contrário dos objetos de retorno de chamada, o CLSID de retorno de chamada será persistido junto com seus respectivos trabalho bits se o serviço BITS ou o sistema for desligado e reiniciado. Seu aplicativo pode limpar qualquer CLSID de notificação definida anteriormente antes de sair (ou em qualquer outro momento) passando uma nova CLSID de notificação de GUID NULL, mas seu aplicativo pode preferir deixar a CLSID de notificação registrada se seu aplicativo tiver registrado para que COM inicie-o em resposta às solicitações \_ coCreateInstance para o CLSID. Observe que, se mais de um aplicativo definir as chamadas à propriedade CLSID DE NOTIFICAÇÃO DE PROPRIEDADE DO TRABALHO DO BITS, o último **\_ \_ \_ \_ CLSID** a ser definido será aquele que o BITS usará para insinuar objetos de retorno de chamada – os outros CLSIDs não serão instanados. Da mesma forma, se um aplicativo registrar um CLSID e outro registrar um objeto de retorno de chamada, as regras usuais para o objeto de retorno de chamada que têm precedência se aplicarão e o CLSID não será usado, a menos que o objeto de retorno de chamada seja limpo ou se torne desconectado.

O exemplo a seguir mostra como se registrar para notificações CLSID. O exemplo pressupo que o ponteiro da interface [**IBackgroundCopyJob5**](/windows/desktop/api/Bits5_0/nn-bits5_0-ibackgroundcopyjob5) é válido e que seu aplicativo já foi registrado como um servidor COM fora do processo que implementa a classe CNotifyInterface. Para obter detalhes sobre a classe de exemplo CNotifyInterface usada no exemplo a seguir, consulte a interface [**IBackgroundCopyCallback.**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopycallback)


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



 

 