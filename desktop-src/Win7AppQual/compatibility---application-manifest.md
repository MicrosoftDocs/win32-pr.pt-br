---
description: Manifesto do aplicativo
ms.assetid: f022374d-ea3f-477f-9b59-3188b775ed64
title: Manifesto do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c52b8eb2af87c271151be3d7989f50b2903084
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088584"
---
# <a name="application-manifest"></a>Manifesto do aplicativo

## <a name="affected-platforms"></a>Plataformas afetadas

**Clientes** -Windows 7  
**Servidores** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto do recurso

 **Severidade** -baixa  
**Frequência** -baixa  





## <a name="description"></a>Descrição

O Windows 7 apresenta uma nova seção no manifesto do aplicativo chamada "Compatibility". Esta seção ajuda o Windows a determinar as versões do Windows que um aplicativo foi projetado para direcionar e permite que o Windows forneça o comportamento que o aplicativo espera com base na versão do Windows de destino do aplicativo.

A seção de compatibilidade permite que o Windows forneça um novo comportamento para o novo software criado pelo desenvolvedor, mantendo a compatibilidade para o software existente. Esta seção também ajuda o Windows a fornecer maior compatibilidade em versões futuras do Windows. Por exemplo, um aplicativo que declara suporte somente para o Windows 7 na seção de compatibilidade continuará a receber o comportamento do Windows 7 na versão futura do Windows.

## <a name="manifestation-of-change"></a>Manifestação de alteração

Os aplicativos sem uma seção de compatibilidade em seu manifesto receberão o comportamento do Windows Vista por padrão no Windows 7 e em versões futuras do Windows. Observe que o Windows XP e o Windows Vista ignoram essa seção de manifesto e não têm nenhum impacto sobre elas.

Os seguintes componentes do Windows fornecem comportamento divergente com base na seção de compatibilidade do Windows 7:

**Pool de threads padrão RPC**

-   **Windows 7:** Para melhorar a escalabilidade e reduzir as contagens de threads, o RPC alternou para o pool de threads NT (pool padrão). Para o Windows Vista, o RPC usava um pool de threads privado.
    -   Para binários compilados para o Win7, o pool padrão é usado
    -   Se I \_ RpcMgmtEnableDedicatedThreadPool for chamado antes de qualquer API RPC ser chamada, o pool de threads privado será usado (comportamento do vista)
    -   Se eu \_ RpcMgmtEnableDedicatedThreadPool for chamado após uma chamada RPC, o pool padrão será usado, I \_ RpcMgmtEnableDedicatedThreadPool retornará o erro 1764 e a operação solicitada não terá suporte
-   **Windows Vista (padrão):** Para binários compilados para o Windows Vista e versões anteriores, o pool privado é usado.

**Bloqueio do DirectDraw**

-   **Windows 7:** Os aplicativos manifestados para o Windows 7 não podem chamar a API de bloqueio em DDRAW para bloquear o buffer de vídeo da área de trabalho principal. Isso resultará em erro, e o ponteiro **NULL** para o primário será retornado. Esse comportamento é imposto mesmo se Gerenciador de Janelas da Área de Trabalho composição não estiver ativada. Os aplicativos compatíveis com o Windows 7 não devem bloquear o buffer de vídeo primário para renderização.
-   **Windows Vista (padrão):** Os aplicativos poderão adquirir um bloqueio no buffer de vídeo primário, pois os aplicativos herdados dependem desse comportamento. A execução do aplicativo é desativada Gerenciador de Janelas da Área de Trabalho.

**BLT (transferência de bloco de bits) do DirectDraw para primário sem janela de recorte**

-   **Windows 7:** Os aplicativos manifestados para o Windows 7 são impedidos de executar BLT para o buffer de vídeo da área de trabalho principal sem uma janela de recorte. Isso resultará em erro e a área de BLT não será renderizada. O Windows impõe esse comportamento mesmo se você não ativar Gerenciador de Janelas da Área de Trabalho composição. Os aplicativos compatíveis com o Windows 7 devem BLT a uma janela de recorte.
-   **Windows Vista (padrão):** Os aplicativos devem ser capazes de Bltr o primário sem uma janela de recorte, pois os aplicativos herdados dependem desse comportamento. A execução desse aplicativo desativa o Gerenciador de Janelas da Área de Trabalho.

**API GetOverlappedResult**

-   **Windows 7:** Resolve uma condição de corrida em que um aplicativo multithread usando GetOverlappedResult pode retornar sem redefinir o evento na estrutura sobreposta, fazendo com que a próxima chamada a essa função retorne prematuramente.
-   **Windows Vista (padrão):** Fornece o comportamento com a condição de corrida na qual os aplicativos podem ter uma dependência. Os aplicativos que desejam evitar essa corrida antes do comportamento do Windows 7 devem aguardar no evento sobreposto e, quando sinalizado, chamar GetOverlappedResult com bWait = = **false**.

**PCA (Assistente de compatibilidade do programa)**

-   **Windows 7:** Aplicativos com a seção de compatibilidade não obterão a mitigação do PCA.
-   **Windows Vista (padrão):** Os aplicativos que não forem instalados corretamente ou falharem durante o tempo de execução em algumas circunstâncias específicas obterão a mitigação do PCA. Para obter mais detalhes, consulte a seção de referência.

## <a name="leveraging-feature-capabilities"></a>Aproveitando os recursos do recurso

Atualize o manifesto do aplicativo com as informações de compatibilidade mais recentes para o suporte do sistema operacional. A seção descreve as adições ao manifesto:

-   **Namespace:** Compatibility. v1 (xmlns = "urn: schemas-microsoft-com: Compatibility. v1" >)

-   **Nome da seção:** Compatibilidade (nova seção)

-   **SupportedOS:** GUID do sistema operacional com suporte-os GUIDs que mapeiam para os sistemas operacionais com suporte são:

    -   {e2011457-1546-43c5-a5fe-008deee3d3f0} para Windows Vista: esse é o valor padrão para o contexto Switchback.
    -   {35138b9a-5d96-4fbd-8e2d-a2440225f93a} para Windows 7: os aplicativos que definem esse valor no manifesto do aplicativo obtêm o comportamento do Windows 7.

    > [!Note]  
    > A Microsoft irá gerar e lançar GUIDs para versões futuras do Windows, conforme necessário.

     

Veja a seguir um exemplo de um manifesto atualizado.

> [!Note]  
> O atributo e os nomes de marca no manifesto do aplicativo diferenciam maiúsculas de minúsculas.

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?> 
  <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--The ID below indicates application support for Windows Vista --> 
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates application support for Windows 7 --> 
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/> 
      </application> 
    </compatibility>
  </assembly>
```



O valor da adição de GUIDs para ambos os sistemas operacionais no exemplo acima é fornecer suporte de nível inferior. Os aplicativos que dão suporte a ambas as plataformas não precisariam de manifestos separados para cada plataforma.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilidade, desempenho, confiabilidade e teste de usabilidade

1.  Testar o aplicativo com a nova seção de compatibilidade e `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` garantir que o aplicativo funcione corretamente usando o comportamento mais recente do Windows 7
2.  Testar o aplicativo com a nova seção de compatibilidade e `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (ou sem essa seção inteiramente) para garantir que o aplicativo funcione corretamente usando os comportamentos do Windows Vista no Windows 7

## <a name="known-issues"></a>Problemas conhecidos

**Incompatibilidade de contexto** Um aplicativo é executado em um contexto do Windows Vista em vez de em um contexto do Windows 7 em um computador que esteja executando uma edição x64 do Windows 7 ou do Windows Server 2008 R2.

**Solução** de As atualizações estão disponíveis para corrigir isso para todas as versões compatíveis com base em x64 do Windows 7 e do Windows Server 2008 R2, bem como para todas as versões compatíveis com base em Itanium do Windows Server 2008 R2. Vá para a página de Suporte da Microsoft para [KB 978637: um aplicativo é executado em um contexto do Windows Vista em vez de em um contexto do Windows 7 em um computador que esteja executando uma edição x64 do Windows 7 ou do Windows Server 2008 R2](https://support.microsoft.com/kb/978637) para obter detalhes adicionais e baixar a versão correta para o seu sistema.

**Diagnóstico de despejo de memória bloqueado**

**Solução** de Vá para a página de Suporte da Microsoft para [KB 976038: exceções que são geradas de um aplicativo executado em uma versão de 64 bits do Windows são ignoradas](https://support.microsoft.com/kb/976038) para obter detalhes adicionais.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [**Função QueryActCtxW**](/windows/win32/api/winbase/nf-winbase-queryactctxw)
-   [Manifesto do UAC](/previous-versions/bb756929(v=msdn.10))
-   [Manifestos de aplicativo para aplicativos do Windows](../sbscs/application-manifests.md)
-   [Gerenciador de Janelas da Área de Trabalho (DWM)](../dwm/dwm-overview.md)
-   [Atualização de incompatibilidade de contexto](https://support.microsoft.com/kb/978637)

 

 
