---
title: Moderador de atividade da área de trabalho
description: Moderador de atividade da área de trabalho
ms.assetid: F1C54DB0-0AFC-4A1B-9697-6CEB519C2663
keywords:
- vida útil da bateria
- em espera conectada
- suspensões
- limitação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b465bbb377a06fdad50d04d5fcf788cb2e687fdf5db852125e4143fd971773d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815416"
---
# <a name="desktop-activity-moderator"></a>Moderador de atividade da área de trabalho

## <a name="platform"></a>Plataforma

**clientes** – Windows 8 


> [!Note]  
> a DAM está presente apenas em computadores cliente Windows 8 que dão suporte à espera conectada. A DAM não está presente em SKUs de servidor.

 

  

> [!Note]  
> Windows os aplicativos da loja criados para Windows 8 não são afetados pela DAM.

 

  
</dl>

## <a name="description"></a>Descrição

Nossos clientes estão mudando para plataformas mais claras, menores e mais móveis para atender às suas necessidades de computação. Como parte da mudança para dispositivos móveis, os usuários se preocupam cada vez mais com a vida útil da bateria de seus dispositivos. o DAM (moderador de atividade da área de trabalho) é um dos vários novos recursos do Windows 8 projetado para garantir vida útil e longa da bateria para dispositivos que dão suporte à espera conectada.

O modo de espera conectado ocorre quando o dispositivo está ligado, mas a tela está desligada. nesse estado de energia, o sistema é tecnicamente sempre "ligado" (para dar suporte a cenários principais como email, VoIP, rede social e mensagens instantâneas com aplicativos da Windows Store). É análogo ao estado em que um telefone inteligente está quando o usuário pressiona o botão de energia.

Dessa forma, o software (incluindo aplicativos e o software do sistema operacional) deve estar bem se comparado durante o modo de espera conectado. A DAM foi criada para suprimir a execução do aplicativo de área de trabalho de forma semelhante ao estado de suspensão (S3 em dispositivos ACPI). Ele faz isso suspendendo ou limitando processos de software de desktop no sistema na entrada em espera conectada. isso permite que os sistemas que dão suporte à espera conectada forneçam uso minimizado de recursos e duração de bateria longa e consistente, permitindo que os aplicativos da Windows Store forneçam as experiências conectadas que prometem.

## <a name="details"></a>Detalhes

O DAM é um driver de modo kernel carregado e inicializado na inicialização do sistema se o sistema der suporte à espera conectada. (Isso é determinado pela avaliação de se o campo AOAC no sistema \_ \_A estrutura de recursos de energia retornada por CallNtPowerInformation está definida como true).

Quando a DAM está habilitada e seu processo de área de trabalho é criado, a DAM adiciona seu processo aos objetos de trabalho gerenciados pelo sistema:

-   Se o processo foi criado na sessão 0, a DAM adicionará o processo a um objeto de trabalho sujeito à **limitação**
-   Se o processo foi criado em uma sessão interativa (sessão 1 ou superior), DAM adiciona o processo a um objeto de trabalho sujeito à **suspensão**

> [!Note]  
> por Windows 8, os objetos de trabalho podem ser aninhados. Isso significa que o uso de objetos de trabalho da DAM não interfere no uso de objetos de trabalho existentes de um aplicativo.

 

Quando a tela estiver ativada, a DAM será desengrenada e não afetará nenhum processo no sistema. Quando o sistema está em espera conectado, dependendo da atividade no sistema, a DAM pode limitar ou suspender processos.

-   Os processos que estão sujeitos à suspensão têm todos os seus threads suspensos (sem permissão para serem executados sob nenhuma circunstância); o estado do aplicativo (memória de processo) é mantido
-   Processos que estão sujeitos ao ciclo de limitação entre SUSPENDED e unsuspended (uma grande maior parte do tempo é gasto no estado suspenso)
    -   lembre-se de que Windows também pode detectar que atividades críticas estão ocorrendo e podem cancelar a suspensão de serviços restritos por períodos mais longos durante essa atividade
    -   Além disso, observe que, enquanto em espera conectada, os sensores e as redes podem não estar disponíveis, portanto, os processos restritos devem ser projetados para serem resilientes a condições de rede inadequadas (para a maioria dos processos, isso não exige nenhuma alteração)

Quando a suspensão de DAM é engrenada ou desativada, a DAM dispara a entrega de uma mensagem do WM \_ POWERBROADCAST para os processos sujeitos à suspensão que aceitou a entrega de mensagens (via chamada à API ou Shim de compatibilidade, descrito posteriormente). Após um atraso de alguns segundos, DAM suspende o processo.

Não há notificações quando a limitação de DAM é engrenada ou desengrenada. Os processos não devem precisar de modificação; os processos continuam funcionando, embora em uma taxa mais lenta.

## <a name="manifestation"></a>Manifestação

Geralmente, os processos são suspensos ou limitados durante o estado de espera conectado. Para a maioria dos aplicativos suspensos, isso deve ser muito semelhante a uma transição S3 suspender/retomar ou S4 hibernar/retomar. As manifestações podem incluir, mas não estão limitadas a inconsistências no tempo de atividade/Runtime versus no momento do relógio de parede, inconsistências no comportamento do temporizador ou alterações dramáticas no estado do sistema operacional antes e após a conclusão da suspensão.

A suspensão e a limitação acontecem como uma unidade (todos os processos suspendêveis são suspensos e dessuspensos em harmonia, e todos os processos que podem ser restringidos são limitados e não são limitados em harmonia), portanto, a comunicação entre dois processos suspensos ou dois processos restritos não representa um problema.

O software que se baseia na comunicação entre processos pode precisar de uma consideração especial:

-   **Comunicação entre os processos na sessão 0 (limitada) e na sessão 1 + (suspenso)** – exemplos incluem ícones de bandeja ou componentes de interface do usuário que representam o estado de serviço atual
-   **Comunicação entre componentes no modo de usuário (sessão 0 ou 1) e drivers (que não são restritos nem suspensos)** – os exemplos incluem serviços que funcionam em nome de um driver

Nesses casos, se a comunicação entre processos não for tratada corretamente, os aplicativos poderão aparecer como suspensos ou sem resposta (embora o usuário possa não ver esse impacto diretamente, pois a tela será desativada quando estiver em espera conectada). Na maioria dos casos, no entanto, os serviços e drivers já devem ser desenvolvidos para serem robustos em relação a problemas de comunicação entre processos.

Os fornecedores que criam software para, ou dependentes, devem considerar como a suspensão do processo afeta os tempos de vida e os Handshakes da conexão. Além disso, como a conectividade de rede pode não estar disponível quando estiver no modo de espera conectado, os desenvolvedores de processos criados na sessão 0 devem ser especialmente cientes de como as conexões de rede intermitentes afetam o processo.

## <a name="solution"></a>Solução

Windows Os aplicativos da loja não são afetados pela DAM. Se seu aplicativo de área de trabalho for afetado pela DAM, você poderá solicitar notificações antes que a suspensão seja engrenada (por exemplo, para salvar o estado ou fechar conexões de rede) usando um destes métodos:

-   Se seu aplicativo tiver uma janela (HWND) e você quiser manipular essas notificações por meio do procedimento de janela, chame [RegisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification) para registrar essas mensagens (ou [UnregisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification) para cancelar o registro). Você pode usar \_ o identificador da janela de notificação de dispositivo \_ \_ no parâmetro flags e passar o HWND da sua janela para o como o parâmetro de destinatário. A mensagem recebida é a mensagem do WM \_ POWERBROADCAST.
-   Se seu aplicativo não tiver uma janela (HWND) ou você desejar um retorno de chamada direto, chame [PowerRegisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification) para registrar essas mensagens (ou [PowerUnregisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification) para cancelar o registro). Você deve usar \_ o retorno de chamada do dispositivo notificar \_ no parâmetro flags e passar um valor do tipo PDEVICE \_ notificar \_ \_ parâmetros de assinatura no parâmetro Recipient.
-   Se seu aplicativo não puder ser recompilado, você poderá optar por receber essas \_ mensagens do WM POWERBROADCAST por meio do [Kit de ferramentas do AppCompat](../win7appqual/application-compatibility-toolkit--act-.md) (usando o Shim PromoteDAM).

A mensagem de suspensão é WM \_ POWERBROADCAST com wParam = PBT \_ APMSUSPEND; esta mensagem é difundida simultaneamente para todos os processos aceitos no sistema. Seu aplicativo deve executar qualquer trabalho no caminho de suspensão de forma rápida e eficiente. O tempo limite após a notificação de difusão é global, não por processo, para que seu processo possa estar contendendo recursos do sistema se o trabalho necessário nesse caminho for extensivo.

A mensagem de retomada é WM \_ POWERBROADCAST com wParam = PBT \_ APMRESUME; esta mensagem é difundida simultaneamente para todos os processos aceitos após um reinício. O tempo relativo de entrega para o sistema sair do modo de espera conectado não é garantido.

Para aplicativos relacionados à câmera, quando a transição de estado de energia está ocorrendo, durante a notificação de suspensão, os aplicativos devem liberar todas as referências à câmera (todos os objetos de pipeline de captura devem ser desligados e descartados).  para evitar uma possível descarga da bateria, em Windows 10 RS3 + systems Câmera do Windows o serviço do servidor de quadros fechará todas as sessões de captura se o aplicativo não tratar a notificação de suspensão corretamente.  O efeito colateral disso é que, quando o sistema sai do estado de espera ou S3/S4, o pipeline de captura do aplicativo não está mais em um estado de funcionamento.

## <a name="tests"></a>Testes

Teste seu software em transições em espera conectadas.

## <a name="resources"></a>Recursos

-   [soluções de vida útil da bateria móvel para o Windows 7](/previous-versions/windows/hardware/design/dn641606(v=vs.85))
-   [\_recursos de energia do sistema \_](/windows/win32/api/winnt/ns-winnt-system_power_capabilities)
-   [Função CallNtPowerInformation](/windows/win32/api/powerbase/nf-powerbase-callntpowerinformation)
-   [Objetos de trabalho](../procthread/job-objects.md)
-   [RegisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-registersuspendresumenotification)
-   [UnregisterSuspendResumeNotification](/windows/win32/api/winuser/nf-winuser-unregistersuspendresumenotification)
-   [PowerRegisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerregistersuspendresumenotification)
-   [PowerUnregisterSuspendResumeNotification](/windows/win32/api/powerbase/nf-powerbase-powerunregistersuspendresumenotification)
-   [Kit de ferramentas AppCompat](../win7appqual/application-compatibility-toolkit--act-.md)

 

 