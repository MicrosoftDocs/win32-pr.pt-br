---
title: Windows Classe auxiliar extensível Filtering Platform
description: O Windows WFP (Plataforma de Filtragem de Dados) inclui uma classe auxiliar NDF (Estrutura de Diagnóstico de Rede), chamada de classe auxiliar da Plataforma de Filtragem (FPHC).
ms.assetid: 006ea30c-8682-4a3d-803a-73dba5162696
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff972beffebb44b33eb68a0439193307639522738ac1f8766845404c03d3cd9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065206"
---
# <a name="windows-filtering-platform-extensible-helper-class"></a>Windows Classe auxiliar extensível Filtering Platform

O [Windows WFP (Plataforma](/windows/desktop/FWP/windows-filtering-platform-start-page) de Filtragem de Dados) inclui uma classe auxiliar Estrutura de Diagnóstico de Rede (NDF), chamada de classe auxiliar da Plataforma de Filtragem (FPHC). O FPHC pode ajudar a identificar as causas raiz dos problemas de conectividade causados pelo WFP. Os desenvolvedores de firewall de terceiros podem implementar suas próprias classes auxiliares de NDF. A extensibilidade de FPHC permite que essas classes auxiliares de terceiros sejam invocadas durante o diagnóstico.

Este tópico pressu parece familiaridade com a [API do WFP.](/windows/desktop/FWP/windows-filtering-platform-start-page)

## <a name="why-extend-the-fphc"></a>Por que estender o FPHC?

Todos os desenvolvedores que escrevem aplicativos que chamam a API do WFP devem escrever uma classe auxiliar NDF que estenda o FPHC.

O FPHC pode identificar o WFP como a causa de um problema de conectividade. Se disponível, o FPHC também pode identificar o provedor que criou o filtro que está bloqueando o tráfego de rede. O FPHC passa essas informações para o NDF, que, por sua vez, pode notificar o usuário de que o WFP está causando o problema de conectividade e dar o nome do provedor bloqueando o tráfego.

No entanto, o FPHC não pode sugerir uma ação corretiva para o usuário, nem pode fornecer o motivo pelo qual o filtro está bloqueando o tráfego para o usuário. Somente uma extensão FPHC pode executar essas tarefas.

Considere um aplicativo de firewall de terceiros que chama a API WFP. Se o firewall de terceiros implementar uma extensão FPHC, ações personalizadas poderão ser implementadas para lidar com problemas de conectividade identificados pelo NDF. Quando o NDF diagnostica que um aplicativo foi bloqueado pelo firewall de terceiros, a extensão FPHC pode manipular o evento de bloqueio. Uma maneira de a extensão FPHC manipular um evento é apresentar ao usuário um prompt para desbloquear um programa usando o firewall e desbloquear o programa após a confirmação do usuário. Como alternativa, a extensão FPHC pode manipular um evento notificando o usuário do motivo pelo qual o aplicativo foi bloqueado, como um aplicativo foi bloqueado porque ele foi considerado malware pelo firewall.

## <a name="about-wfp-diagnostics"></a>Sobre o diagnóstico do WFP

Quando o NDF é invocado para diagnosticar um problema de rede, as classes auxiliares são contatadas para determinar a causa do problema. Se uma classe auxiliar de nível superior determinar que uma falha de rede pode ser causada pelo WFP, ela gerará uma hipótese para FPHC com base nas informações disponíveis. O NDF passa essa hipótese, na forma de vários atributos de evento, para FPHC. Esses atributos são descritos em detalhes na seção Atributos de Evento [FPHC](#windows-filtering-platform-extensible-helper-class) abaixo.

Um problema de rede pode ser descrito como um problema de conectividade que afeta uma tentativa de conexão específica. Por exemplo, o usuário pode ter bloqueado acidentalmente um aplicativo clicando inadvertidamente **em Não permitir**. Em seguida, o firewall bloqueará a associação do aplicativo a qualquer porta. O usuário, sem saber por que o aplicativo está bloqueado, pode tentar diagnosticar o problema por meio de um ponto de entrada oferecido pelo aplicativo. O FPHC olhará os logs e, se encontrar uma combinação, ele recuperará a ID do filtro e a ID do provedor desse filtro específico. Neste ponto, o FPHC sabe quem é o proprietário desse filtro e entregará o processo de diagnóstico para a classe auxiliar apropriada para diagnóstico posterior.

O evento mais recente nos logs de eventos do WFP para corresponder aos atributos é selecionado como sendo relevante para o problema de rede. Se nenhum evento correspondente for encontrado e a hora em que o evento ocorreu for abordada no log do WFP, o FPHC indicará ao NDF que ele está oso. Se nenhum evento correspondente for encontrado e os logs do WFP não incluírem a hora em que o evento ocorreu, o FPHC retornará um status indeterminado para o NDF.

Se um evento correspondente for encontrado, o FPHC usará a ID do provedor do filtro que fez com que o evento identificasse o provedor da regra de segurança que bloqueou a conectividade. Em seguida, o FPHC verifica se existe uma extensão de classe auxiliar para esse provedor. Se uma for encontrada, o FPHC gerará uma hipótese para esse provedor e, em seguida, o NDF invocará a extensão. A extensão deve retornar informações úteis de diagnóstico e reparo para o usuário.

## <a name="helper-class-registration"></a>Registro de classe auxiliar

Uma extensão FPHC deve ser registrada conforme descrito em [Registrando extensões de classe auxiliar NDF](registering-ndf-helper-class-extensions.md). Os desenvolvedores que implementam uma classe auxiliar devem registrar suas extensões para garantir que a extensão seja chamada pelo NDF quando apropriado. O  atributo correspondente descrito abaixo deve ser armazenado no Registro em **HKLM \\ \\ System CurrentControlSet \\ Control \\ NetDiagFx** \\ *VendorName* \\ **HostDLLs** Helper Class \\ *DLL* \\ **HelperClasses Helper** Class Name \\  \\ **MatchAttributes**.

A tabela a seguir mostra o atributo correspondente usado para identificar a hipótese a ser usada no diagnóstico no log de eventos do WFP. 

| Nome       | Tipo    | Descrição                                                                                                                                                                                                                                                                                                 |
|------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Providerid | REG \_ SZ | O GUID da extensão FPHC. Esse valor deve ser o mesmo que o GUID do provedor WFP. <br/> Essa cadeia de caracteres faz a resiência de minúsculas. Ele deve ser armazenado no Registro em letras maiúsculas com chaves e hifens delimitadores. Por exemplo, {C200E360-38C5-11CE-AE62-08002B2B79EF} é um ProviderID válido.<br/> |



 

Quando o ProviderID de um filtro de bloqueio corresponde ao de uma classe auxiliar registrada, o FPHC informa ao NDF para invocar essa classe auxiliar, estendendo assim a funcionalidade de diagnóstico de FPHC.

## <a name="fphc-event-attributes"></a>Atributos de evento FPHC

A tabela a seguir lista os atributos de evento associados a cada evento correspondente. Cada atributo de evento é armazenado em uma [**estrutura HELPER \_ ATTRIBUTE.**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) Esses atributos são passados por NDF para FPHC quando um evento correspondente é encontrado. Eles podem, por sua vez, ser passados para extensões FPHC.



| Atributo     | [**ATRIBUTO \_ Valor TYPE**](/windows/win32/api/ndattrib/ne-ndattrib-attribute_type) | Descrição                                                                                                                               |
|---------------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| GUID do provedor | NO \_ GUID                                        | O GUID do provedor associado ao filtro.                                                                                      |
| Timestamp     | EM \_ CADEIA DE CARACTERES OCTETO \_                               | Um buffer do tipo FILETIME que especifica a hora em que o evento ocorreu. Esse carimbo de data/hora pode ser usado para identificar exclusivamente um evento. |
| ipProtocol    | AT \_ UINT32                                      | O protocolo de camada de transporte, no formato UINT8.                                                                                            |
| Localaddr     | AT \_ SOCKADDR                                    | O endereço IP local e a porta, armazenados em [**uma estrutura \_ DIAG SOCKADDR.**](/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr)                                             |
| RemoteAddr    | AT \_ SOCKADDR                                    | O endereço IP remoto e a porta, armazenados em [**uma estrutura \_ DIAG SOCKADDR.**](/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr)                                            |
| userId        | EM \_ CADEIA DE CARACTERES OCTETO \_                               | Um buffer do tipo SID que representa o userid. Se userId for de comprimento 0, o SID não estará disponível.                                        |
| appId         | AT \_ STRING                                      | Um buffer que armazena o identificador do aplicativo recuperado. Se appId tiver um valor de L"", o identificador do aplicativo não estará disponível.        |



 

## <a name="handling-fphc-events"></a>Manipulando eventos FPHC

Antes de sugerir informações de diagnóstico e reparo para o usuário, uma extensão FPHC deve coletar mais dados do que o fornecido pelas notificações FPHC. Esses dados podem ser adquiridos das Funções de Gerenciamento de Eventos [do WFP.](/windows/desktop/FWP/fwp-mgmt-functions) Essas funções são demonstradas no exemplo [Exibindo Eventos Líquidos.](/windows/desktop/FWP/displaying-net-events)

Um exemplo de gerenciamento de eventos mais detalhado está incluído no SDK. O código-fonte do exemplo pode ser encontrado no local de instalação do SDK em C: Arquivos de Programas \\ \\ SDKs da Microsoft Windows \\ \\ <version number> \\ \\ Exemplos de \\ NetDs WFP \\ DiagEvents. O Windows SDK do Vista está disponível no Centro [de Download.](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf)

## <a name="built-in-fphc-diagnostics"></a>Diagnóstico de FPHC integrado

Na ausência de uma extensão FPHC, o FPHC pode diagnosticar os cenários listados abaixo. A maioria das falhas de conectividade diagnosticadas pelo FPHC ocorre porque os firewalls bloqueiam o tráfego. Os cenários de IPsec são menos comuns.

A tabela a seguir mostra alguns cenários que causam falhas de conectividade que podem ser diagnosticadas pelo FPHC, juntamente com as informações de descrição e reparo passadas para o NDF.



| Cenário                   | Descrição de baixa saúde                                                                                                               | Reparar informações                   |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Redução do firewall              | As configurações de firewall neste computador estão bloqueando a conexão.                                                                  | Verifique as configurações de firewall.       |
| Falha no modo principal          | Você não pode se conectar devido a uma incompatibilidade de política de segurança IPsec.                                                                     | Entre em contato com o proprietário da política IPsec.      |
| Falha no modo rápido         | Você não pode se conectar devido a uma incompatibilidade de política de segurança IPsec.                                                                     | Entre em contato com o proprietário da política IPsec.      |
| Falha no modo de usuário          | Você não pode se conectar devido a uma incompatibilidade de política de segurança IPsec.                                                                     | Entre em contato com o proprietário da política IPsec.      |
| Falha de credencial         | Você não pode se conectar porque a AC (autoridade de certificação) raiz neste computador não corresponderá à AC raiz no computador remoto. | Atualize o certificado raiz confiável. |
| Certificado expirado        | O certificado usado para autenticação IPsec expirou.                                                                           | Solicitar um certificado.               |
| Outras falhas de certificado | Um certificado válido não foi encontrado para autenticação IPsec.                                                                          | Solicitar um certificado.               |
| Falha de Kerberos           | O computador não faz parte desse domínio.                                                                                             | Ingressar este computador em um domínio.      |
| Chave pré-compartilhada              | Redefinir as chaves pré-compartilhadas.                                                                                                            | Redefinir as chaves pré-compartilhadas.            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Plataforma de filtragem do Windows](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[Projetando extensões de classe auxiliar do NDF](designing-ndf-helper-class-extensions.md)
</dt> <dt>

[Registrando extensões de classe auxiliar do NDF](registering-ndf-helper-class-extensions.md)
</dt> <dt>

[Exemplos de classe auxiliar do NDF](ndf-helper-class-examples.md)
</dt> </dl>

 

