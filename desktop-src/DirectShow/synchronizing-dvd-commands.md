---
description: Sincronizando comandos de DVD
ms.assetid: 37e8f940-617d-43f6-92bd-aadccafe0059
title: Sincronizando comandos de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d677c38363a0ab80f90f58498eeef24bdc29eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785333"
---
# <a name="synchronizing-dvd-commands"></a>Sincronizando comandos de DVD

Os comandos de DVD nem sempre são concluídos instantaneamente. Por esse motivo, alguns dos métodos em [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) são assíncronos. Isso inclui métodos de reprodução, como **PlayTitle** e métodos de navegação de menu, como o **menu** de menus e **ReturnFromSubmenu**. Um método assíncrono retorna imediatamente, sem esperar que o comando seja concluído. Depois que o método retornar, outros eventos poderão impedir a conclusão do comando, mesmo se o método tiver sido bem-sucedido. O DirectShow fornece várias opções de sincronização de comandos, variando de nenhuma sincronização à sincronização completa usando eventos de gráfico de filtro.

Todos os métodos assíncronos têm um parâmetro *dwFlags* e um parâmetro *ppCmd* . O parâmetro *dwFlags* especifica o comportamento de sincronização e o parâmetro *ppCmd* retorna um ponteiro para um objeto de sincronização opcional. Comportamentos diferentes resultam de acordo com os valores que você fornece para esses parâmetros.

**Sem sincronização**

Para um aplicativo de reprodução de DVD básico, a melhor opção pode ser simplesmente ignorar problemas de sincronização. Ocasionalmente, um comando pode falhar ou a interface do usuário pode atrasar um pouco quando é atualizada, mas esses erros estarão na ordem de frações de segundos.

Para emitir um comando sem sincronização, defina o sinalizador DVD \_ cmd \_ Flag \_ None no parâmetro *dwFlags* e defina o parâmetro *ppCmd* como **NULL**:


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, NULL);
```



**Bloqueio**

Se você definir o \_ sinalizador de bloco de sinalizadores de DVD do EC \_ \_ \_ no parâmetro *dwFlags* , o método será bloqueado até que o comando seja concluído:


```C++
hr = pDVDControl2->PlayTitle(uTitle, EC_DVD_CMD_FLAG_Block, NULL);
```



Na verdade, esse sinalizador transforma um método assíncrono em um método síncrono. A desvantagem é que sua interface do usuário será bloqueada se você chamar o método do thread do aplicativo.

**Objeto de sincronização**

Todos os métodos assíncronos podem retornar um objeto de sincronização, que você pode usar para aguardar até que o comando inicie ou termine. Para obter esse objeto, passe o endereço de um ponteiro [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) no parâmetro *ppCmd* :


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
```



Se o método tiver sucesso, ele retornará um novo objeto **IDvdCmd** . O método [**IDvdCmd:: WaitForStart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) é bloqueado até que o comando comece e o método [**IDvdCmd:: WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) seja bloqueado até que o comando termine. O valor de retorno indica o status do comando.

O código a seguir é funcionalmente equivalente a definir o \_ sinalizador de bloco de sinalizadores de DVD do EC \_ \_ \_ , mostrado anteriormente.


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
if (SUCCEEDED(hr))
{
    // Use pCmdObj to wait for the command to complete.
    hr = pCmdObj->WaitToEnd();
    pCmdObj->Release();
}
```



Nesse caso, o método **PlayTitle** não bloqueia, mas os blocos de aplicativo chamando **WaitForEnd**.

**Eventos de status de comando**

Se você definir o \_ sinalizador SendEvents de DVD cmd Flag \_ \_ no parâmetro *dwFlags* , o DVD Navigator enviará um evento de início de [**cmd de DVD EC quando o comando \_ \_ \_ for**](ec-dvd-cmd-start.md) iniciado e um evento de término de [**\_ cmd de DVD \_ \_ EC**](ec-dvd-cmd-end.md) quando o comando terminar.

O parâmetro *lParam2* do evento é o valor de retorno HRESULT para o comando. O parâmetro *lParam1* do evento fornece uma maneira de obter o objeto de sincronização para o comando. Se você passar *lParam1* para o método [**IDvdInfo2:: GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) , o método retornará um ponteiro para a interface **IDvdCmd** do objeto de sincronização. Você pode usar essa interface para aguardar a conclusão do comando, conforme descrito anteriormente. No entanto, se você tiver passado **nulo** para o parâmetro *PpCmd* no método **IDvdControl2** original, o DVD Navigator não criará um objeto de sincronização e **GetCmdFromEvent** retornará e \_ falhará.

O código a seguir mostra como usar eventos de status de comando sem objeto de sincronização.


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, NULL);

// In your event handling code:
switch (lEvent)
{
   case EC_DVD_CMD_END:
       HRESULT hr2 = (HRESULT)lParam2;
       /* ... */ 
       break;
}
```



Observe que, sem um objeto de sincronização, você não pode saber qual comando está associado ao evento. O código a seguir mostra como usar eventos com o objeto de sincronização. A ideia é armazenar os objetos de sincronização em uma lista e, em seguida, comparar os ponteiros de objeto ao obter o evento de encerramento de cmd de [**\_ DVD EC \_ \_**](ec-dvd-cmd-start.md) ou de [**\_ \_ \_ fechamento de DVD EC**](ec-dvd-cmd-end.md) .


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, &pCmdObj);
if (SUCCEEDED(hr)) 
{
    // Store pCmdObj in a list of pending commands.
}

// In your event handling code:
switch (lEvent)
{
case EC_DVD_CMD_END:
   {
       IDvdCmd *pObj = NULL;
       hr = pDvdInfo2->GetCmdFromEvent(lParam, &pObj);
       if (SUCCEEDED(hr)) 
       {
           // Find this object in your list by comparing IUnknown
           // pointers. Assume the following function is defined in 
           // your application:
           IDvdCmd *pPendingObj = GetPendingCommandFromList(pObj); 
           if (pPendingObj)
           {
               // Update UI accordingly (not shown). 
               pPendingObj->Release();
           }
           pObj->Release();
       }
    }
    break;
} 
```



**Liberando os buffers do navegador de DVD**

Durante a reprodução, o navegador de DVD armazena em buffer os dados de vídeo. A quantidade de dados em buffer varia. Quando o navegador de DVD alterna para um novo vídeo, os dados que já estão no pipeline não são perdidos e, portanto, a transição é direta. Por padrão, quando o navegador de DVD emite um comando, ele não libera os dados que já estão no pipeline. Como resultado, pode haver alguma latência antes que você possa ver o efeito do comando, dependendo da quantidade de dados armazenada em buffer. Para aumentar a capacidade de resposta, você pode forçar a liberação do navegador de DVD definindo o \_ sinalizador de liberação do sinalizador de DVD cmd \_ \_ .


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_Flush, NULL);
```



Esse sinalizador pode ser combinado com qualquer um dos sinalizadores descritos anteriormente, usando um OR bit a bit. Um efeito colateral da liberação é que algum vídeo pode ser perdido, portanto, não use esse sinalizador se você precisar garantir que não haja lacunas no vídeo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicativos de DVD](dvd-applications.md)
</dt> </dl>

 

 



