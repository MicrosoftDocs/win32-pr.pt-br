---
description: Códigos de notificação de eventos de DVD
ms.assetid: c028918e-aba2-49b2-a6ce-c620ab38b558
title: Códigos de notificação de eventos de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e15172e8eba3da048e7c7704a90d7992fa21714a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105759079"
---
# <a name="dvd-event-notification-codes"></a>Códigos de notificação de eventos de DVD

Esta seção lista os códigos de notificação de eventos para reprodução e navegação em DVD no DirectShow.

Para obter informações sobre como receber eventos no DirectShow, consulte [notificação de eventos no DirectShow](event-notification-in-directshow.md).

Para outros códigos de eventos não-DVD, consulte [códigos de notificação de eventos](event-notification-codes.md).



| Código de notificação de eventos                                                        | Descrição                                                                                                                                                               |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_alteração de \_ ângulo do DVD do EC \_**](ec-dvd-angle-change.md)                          | Sinaliza que o número de ângulos disponíveis foi alterado ou que o número de ângulo atual foi alterado.                                                                      |
| [**ângulos de DVD do EC \_ \_ \_ disponíveis**](ec-dvd-angles-available.md)                  | Indica se um bloco de ângulo está sendo reproduzido e se as alterações de ângulo podem ser executadas.                                                                                      |
| [**\_alteração de \_ fluxo de áudio \_ \_ do EC DVD**](ec-dvd-audio-stream-change.md)           | Sinaliza que o número do fluxo de áudio atual foi alterado para o título principal.                                                                                                  |
| [**\_BeginNavigationCommands de DVD do EC \_**](ec-dvd-beginnavigationcommands.md)     | Enviado quando um conjunto de comandos de navegação de DVD está sendo iniciado.                                                                                                                  |
| [**\_botão de DVD EC \_ \_ \_ ativado automaticamente**](ec-dvd-button-auto-activated.md)       | Sinaliza que um botão de menu foi ativado automaticamente por instruções no disco.                                                                                 |
| [**\_alteração do \_ botão de DVD do EC \_**](ec-dvd-button-change.md)                        | Sinaliza que o número de botões disponíveis foi alterado ou que o número do botão selecionado atualmente foi alterado.                                                         |
| [**\_ \_ capítulo \_ autostop do DVD do EC**](ec-dvd-chapter-autostop.md)                  | Indica que a reprodução parou como resultado de uma chamada para o método [**IDvdControl2::P laychaptersautostop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchaptersautostop) .                    |
| [**início do capítulo do EC \_ DVD \_ \_**](ec-dvd-chapter-start.md)                        | Sinaliza que o navegador de DVD iniciou a reprodução de um novo capítulo no título atual.                                                                                    |
| [**\_início do \_ cmd de DVD do EC \_**](ec-dvd-cmd-start.md)                                | Sinaliza que um comando específico foi iniciado.                                                                                                                              |
| [**\_fim do \_ cmd de DVD do EC \_**](ec-dvd-cmd-end.md)                                    | Sinaliza que um comando específico foi concluído.                                                                                                                          |
| [**\_hora de \_ \_ HMSF atual do DVD \_ do EC**](ec-dvd-current-hmsf-time.md)               | Sinaliza a hora atual no formato de [**\_ \_ código**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) de tempo HMSF do DVD no início de cada VOBU (unidade de objeto de vídeo).                                   |
| [**\_ \_ hora atual do DVD do EC \_**](ec-dvd-current-time.md)                          | Sinaliza o início de cada VOBU.                                                                                                                                      |
| [**\_disco DVD do EC \_ \_ ejetado**](ec-dvd-disc-ejected.md)                          | Sinaliza que um disco foi ejetado da unidade.                                                                                                                      |
| [**\_disco de DVD EC \_ \_ inserido**](ec-dvd-disc-inserted.md)                        | Sinaliza que um disco foi inserido na unidade.                                                                                                                     |
| [**\_alteração de \_ domínio de DVD do EC \_**](ec-dvd-domain-change.md)                        | Indica o novo domínio do navegador de DVD.                                                                                                                                 |
| [**\_erro de DVD do EC \_**](ec-dvd-error.md)                                         | Sinaliza uma condição de erro de DVD.                                                                                                                                            |
| [**\_Alteração de \_ GPRM de DVD do EC \_**](ec-dvd-gprm-change.md)                            | Enviado quando o valor de um registro de parâmetro geral (GPRM) é alterado.                                                                                                       |
| [**\_modo de \_ karaokê de DVD do EC \_**](ec-dvd-karaoke-mode.md)                          | Indica que o navegador começou a reproduzir ou terminou de reproduzir dados do karaokê.                                                                                   |
| [**\_NavigationCommand de DVD do EC \_**](ec-dvd-navigationcommand.md)                 | Enviado quando o [navegador de DVD](dvd-navigator-filter.md) processa um comando de navegação de DVD.                                                                               |
| [**DVD do EC \_ \_ sem \_ FP \_ PGC**](ec-dvd-no-fp-pgc.md)                               | Indica que o disco DVD não tem um FP \_ PGC (primeira cadeia de programas de reprodução).                                                                                           |
| [**\_alteração no \_ nível do pai do DVD do EC \_ \_**](ec-dvd-parental-level-change.md)       | Sinaliza que o nível pai do conteúdo criado está prestes a ser alterado.                                                                                               |
| [**\_alteração da \_ taxa de reprodução de DVD do EC \_ \_**](ec-dvd-playback-rate-change.md)         | Indica que uma alteração de taxa de reprodução foi iniciada e a nova taxa está no parâmetro.                                                                            |
| [**reprodução de DVD do EC \_ \_ \_ interrompida**](ec-dvd-playback-stopped.md)                  | Indica que a reprodução foi interrompida. O navegador de DVD concluiu a reprodução do título e não encontrou nenhuma outra instrução de ramificação para reprodução subsequente. |
| [**autoparada de PLAYPERIOD do EC \_ DVD \_ \_**](ec-dvd-playperiod-autostop.md)            | Indica que o navegador terminou de reproduzir o segmento especificado em uma chamada para PlayPeriodInTitleAutoStop.                                                           |
| [**\_alteração de \_ célula do programa de DVD do EC \_ \_**](ec-dvd-program-cell-change.md)           | Enviado quando o número do programa de DVD ou o número da célula é alterado.                                                                                                                  |
| [**\_alteração da \_ cadeia de programas \_ \_ do EC DVD**](ec-dvd-program-chain-change.md)         | Enviado quando a cadeia de programa atual (PGC) é alterada.                                                                                                                            |
| [**\_Alteração de \_ SPRM de DVD do EC \_**](ec-dvd-sprm-change.md)                            | Enviado quando o valor de um SPRM (registro de parâmetro do sistema) é alterado.                                                                                                        |
| [**o \_ DVD do EC \_ ainda está \_ desativado**](ec-dvd-still-off.md)                                | Sinaliza o final de qualquer ainda.                                                                                                                                             |
| [**o \_ DVD \_ do EC ainda está \_ ativado**](ec-dvd-still-on.md)                                  | Sinaliza o início de qualquer ainda.                                                                                                                                       |
| [**\_alteração de \_ fluxo de subimagem do DVD do \_ EC \_**](ec-dvd-subpicture-stream-change.md) | Sinaliza que o número de fluxo da subimagem atual foi alterado para o título principal.                                                                                             |
| [**\_alteração de \_ definição de título de DVD do EC \_ \_**](ec-dvd-title-set-change.md)                 | Enviado quando o conjunto de títulos de vídeo atual (VTS) é alterado.                                                                                                                          |
| [**\_alteração do \_ título do DVD do EC \_**](ec-dvd-title-change.md)                          | Indica quando o número do título atual é alterado.                                                                                                                          |
| [**\_ \_ \_ alteração UOPS válida do DVD do EC \_**](ec-dvd-valid-uops-change.md)               | Sinaliza que o conjunto disponível de métodos de interface [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) foi alterado.                                                                     |
| [**\_Deslocamento de \_ VOBU de DVD do EC \_**](ec-dvd-vobu-offset.md)                            | Enviado quando o [navegador de DVD](dvd-navigator-filter.md) analisa um pacote PCI.                                                                                              |
| [**\_Carimbo de \_ \_ data/hora VOBU do EC DVD**](ec-dvd-vobu-timestamp.md)                      | Enviado quando o [navegador de DVD](dvd-navigator-filter.md) analisa um pacote PCI.                                                                                              |
| [**\_aviso de DVD do EC \_**](ec-dvd-warning.md)                                     | Sinaliza uma condição de aviso de DVD.                                                                                                                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes e GUIDs](constants-and-guids.md)
</dt> </dl>

 

 



