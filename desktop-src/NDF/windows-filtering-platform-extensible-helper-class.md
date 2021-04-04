---
title: Classe auxiliar extensível da plataforma de filtragem do Windows
description: A WFP (plataforma de filtragem do Windows) inclui uma classe auxiliar NDF (estrutura de diagnóstico de rede), chamada de FPHC (classe auxiliar de plataforma de filtragem).
ms.assetid: 006ea30c-8682-4a3d-803a-73dba5162696
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858835c1a649602293ed042c13205ca982de9258
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917384"
---
# <a name="windows-filtering-platform-extensible-helper-class"></a>Classe auxiliar extensível da plataforma de filtragem do Windows

A [WFP (plataforma de filtragem do Windows)](/windows/desktop/FWP/windows-filtering-platform-start-page) inclui uma classe auxiliar NDF (estrutura de diagnóstico de rede), chamada de FPHC (classe auxiliar de plataforma de filtragem). O FPHC pode ajudar a identificar as causas raiz dos problemas de conectividade causados pela WFP. Os desenvolvedores de firewall de terceiros podem implementar suas próprias classes auxiliares NDF. A extensibilidade do FPHC permite que essas classes auxiliares de terceiros sejam invocadas durante o diagnóstico.

Este tópico pressupõe familiaridade com a [API WFP](/windows/desktop/FWP/windows-filtering-platform-start-page).

## <a name="why-extend-the-fphc"></a>Por que estender o FPHC?

Todos os desenvolvedores que escrevem aplicativos que chamam a API WFP devem gravar uma classe auxiliar NDF que estenda FPHC.

O FPHC pode identificar a WFP como a causa de um problema de conectividade. Se disponível, o FPHC também pode identificar o provedor que criou o filtro que está bloqueando o tráfego de rede. O FPHC passa essas informações para o NDF, que, por sua vez, pode notificar o usuário de que a WFP está causando o problema de conectividade e dar o nome do provedor que está bloqueando o tráfego.

No entanto, o FPHC não pode sugerir uma ação corretiva para o usuário, nem pode fornecer o motivo pelo qual o filtro está bloqueando o tráfego para o usuário. Somente uma extensão FPHC pode executar essas tarefas.

Considere um aplicativo de firewall de terceiros que chama a API WFP. Se o firewall de terceiros implementar uma extensão FPHC, as ações personalizadas poderão ser implementadas para lidar com problemas de conectividade identificados pelo NDF. Quando o NDF diagnostica que um aplicativo foi bloqueado pelo firewall de terceiros, a extensão FPHC pode manipular o evento de bloqueio. Uma maneira que a extensão FPHC poderia manipular um evento é apresentar ao usuário um prompt para desbloquear um programa usando o firewall e, em seguida, desbloquear o programa após a confirmação do usuário. Como alternativa, a extensão FPHC poderia lidar com um evento notificando o usuário do motivo pelo qual o aplicativo foi bloqueado, como um aplicativo foi bloqueado porque ele foi considerado malware pelo firewall.

## <a name="about-wfp-diagnostics"></a>Sobre o diagnóstico de WFP

Quando o NDF é invocado para diagnosticar um problema de rede, as classes auxiliares são contatadas para determinar a causa do problema. Se uma classe auxiliar de nível superior determinar que uma falha de rede pode ser causada pela WFP, ela gerará uma hipótese para FPHC com base nas informações disponíveis. O NDF passa essa hipótese, na forma de vários atributos de evento, para FPHC. Esses atributos são descritos detalhadamente na seção [atributos de evento FPHC](#windows-filtering-platform-extensible-helper-class) abaixo.

Um problema de rede pode ser descrito como um problema de conectividade que afeta uma tentativa de conexão específica. Por exemplo, o usuário pode ter bloqueado acidentalmente um aplicativo clicando inadvertidamente em **não permitir**. Em seguida, o Firewall bloqueará a associação do aplicativo a qualquer porta. O usuário, sem saber por que o aplicativo está bloqueado, pode tentar diagnosticar o problema por meio de um ponto de entrada oferecido pelo aplicativo. FPHC examinará os logs e, se encontrar uma correspondência, recuperará a ID do filtro e a ID do provedor desse filtro específico. Neste ponto, FPHC sabe quem é o proprietário do filtro e ele passará pelo processo de diagnóstico para a classe auxiliar apropriada para diagnóstico mais detalhado.

O evento mais recente nos logs de eventos de WFP para corresponder aos atributos é selecionado como sendo relevante para o problema de rede. Se nenhum evento correspondente for encontrado e a hora em que o evento ocorreu for abordada no log WFP, FPHC indicará ao NDF que ele está íntegro. Se nenhum evento correspondente for encontrado e os logs de WFP não incluírem a hora em que o evento ocorreu, FPHC retornará um status indeterminado para NDF.

Se um evento correspondente for encontrado, FPHC usará a ID do provedor do filtro que fez com que o evento identificasse o provedor da regra de segurança que bloqueou a conectividade. FPHC verifica se existe uma extensão de classe auxiliar para esse provedor. Se um for encontrado, FPHC gerará uma hipótese para esse provedor e, em seguida, NDF invocará a extensão. A extensão deve retornar informações úteis de diagnóstico e reparo para o usuário.

## <a name="helper-class-registration"></a>Registro de classe auxiliar

Uma extensão FPHC deve ser registrada conforme descrito em [registrando extensões de classe auxiliar NDF](registering-ndf-helper-class-extensions.md). Os desenvolvedores que implementam uma classe auxiliar devem registrar suas extensões para garantir que a extensão seja chamada pelo NDF quando apropriado. O *atributo correspondente* descrito abaixo deve ser armazenado no registro em **HKLM \\ sistema \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *nome_do_fornecedorname* \\ **HostDLLs** \\ *auxiliar Class dll* \\ **HelperClasses** \\ *nome da classe auxiliar* \\ **MatchAttribute**.

A tabela a seguir mostra o atributo de correspondência usado para identificar a hipótese a ser usada no diagnóstico no log de eventos do WFP. 

| Nome       | Tipo    | Descrição                                                                                                                                                                                                                                                                                                 |
|------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ProviderID | REG \_ sz | O GUID da extensão FPHC. Esse valor deve ser o mesmo que o GUID do provedor WFP. <br/> Essa cadeia de caracteres diferencia maiúsculas de minúsculas. Ele deve ser armazenado no registro em maiúsculas com chaves e hifens delimitadores. Por exemplo, {C200E360-38C5-11CE-AE62-08002B2B79EF} é uma ProviderID válida.<br/> |



 

Quando o ProviderId de um filtro de bloqueio corresponde ao de uma classe auxiliar registrada, o FPHC informa o NDF para invocar essa classe auxiliar, estendendo, assim, a capacidade de diagnóstico do FPHC.

## <a name="fphc-event-attributes"></a>Atributos de evento FPHC

A tabela a seguir lista os atributos de evento associados a cada evento correspondente. Cada atributo de evento é armazenado em uma estrutura de [**\_ atributo auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) . Esses atributos são passados por NDF para FPHC quando um evento correspondente é encontrado. Por sua vez, eles podem ser passados para extensões FPHC.



| Atributo     | [**Atributo \_**](/windows/win32/api/ndattrib/ne-ndattrib-attribute_type) Valor do tipo | Descrição                                                                                                                               |
|---------------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| GUID do provedor | NO \_ GUID                                        | O GUID do provedor associado ao filtro.                                                                                      |
| Timestamp     | \_cadeia de \_ caracteres de octeto                               | Um buffer do tipo FILETIME que especifica a hora em que o evento ocorreu. Esse carimbo de data/hora pode ser usado para identificar exclusivamente um evento. |
| ipProtocol    | EM \_ UINT32                                      | O protocolo de camada de transporte, no formato UINT8.                                                                                            |
| LocalAddr     | EM \_ SOCKADDR                                    | O endereço IP local e a porta, armazenados em uma estrutura de [**\_ SOCKADDR de diagnóstico**](/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr) .                                             |
| RemoteAddr    | EM \_ SOCKADDR                                    | O endereço IP remoto e a porta, armazenados em uma estrutura de [**\_ SOCKADDR de diagnóstico**](/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr) .                                            |
| userId        | \_cadeia de \_ caracteres de octeto                               | Um buffer do tipo SID que representa o userid. Se userId tiver comprimento 0, o SID não estará disponível.                                        |
| appId         | na \_ cadeia de caracteres                                      | Um buffer que armazena o identificador do aplicativo recuperado. Se appId tiver um valor de L "", o identificador do aplicativo não estará disponível.        |



 

## <a name="handling-fphc-events"></a>Manipulando eventos FPHC

Antes de sugerir informações de diagnóstico e reparo para o usuário, uma extensão FPHC deve coletar mais dados do que é fornecido pelas notificações do FPHC. Esses dados podem ser adquiridos das [funções de gerenciamento de eventos de WFP](/windows/desktop/FWP/fwp-mgmt-functions). Essas funções são demonstradas no exemplo de [exibição de eventos de rede](/windows/desktop/FWP/displaying-net-events) .

Um exemplo de gerenciamento de eventos mais detalhado está incluído no SDK. O código-fonte do exemplo pode ser encontrado no local de instalação do SDK em C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ <version number> \\ Samples \\ NetDs \\ WFP \\ DiagEvents. O SDK do Windows Vista está disponível no [centro de download](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).

## <a name="built-in-fphc-diagnostics"></a>Diagnóstico de FPHC interno

Na ausência de uma extensão FPHC, o FPHC pode diagnosticar os cenários listados abaixo. A maioria das falhas de conectividade diagnosticadas pelo FPHC ocorre porque os firewalls bloqueiam o tráfego. Os cenários de IPsec são menos comuns.

A tabela a seguir mostra alguns cenários que causam falhas de conectividade que podem ser diagnosticadas pelo FPHC, juntamente com a descrição e as informações de reparo passadas para o NDF.



| Cenário                   | Descrição de integridade baixa                                                                                                               | Informações de reparo                   |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Remoção de firewall              | As configurações de firewall neste computador estão bloqueando a conexão.                                                                  | Verifique as configurações do firewall.       |
| Falha no modo principal          | Não é possível se conectar devido a uma incompatibilidade de diretiva de segurança IPsec.                                                                     | Contate o proprietário da política IPsec.      |
| Falha no modo rápido         | Não é possível se conectar devido a uma incompatibilidade de diretiva de segurança IPsec.                                                                     | Contate o proprietário da política IPsec.      |
| Falha no modo de usuário          | Não é possível se conectar devido a uma incompatibilidade de diretiva de segurança IPsec.                                                                     | Contate o proprietário da política IPsec.      |
| Falha de credencial         | Você não pode se conectar porque a AC (autoridade de certificação) raiz neste computador não corresponde à AC raiz no computador remoto. | Atualize o certificado raiz confiável. |
| Certificado expirado        | O certificado usado para autenticação IPsec expirou.                                                                           | Solicitar um certificado.               |
| Outras falhas de certificado | Um certificado válido não foi encontrado para autenticação IPsec.                                                                          | Solicitar um certificado.               |
| Falha de Kerberos           | O computador não faz parte deste domínio.                                                                                             | Ingresse este computador em um domínio.      |
| Chave pré-compartilhada              | Redefina as chaves pré-compartilhadas.                                                                                                            | Redefina as chaves pré-compartilhadas.            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Plataforma de filtragem do Windows](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[Criando extensões de classe auxiliar NDF](designing-ndf-helper-class-extensions.md)
</dt> <dt>

[Registrando extensões de classe auxiliar NDF](registering-ndf-helper-class-extensions.md)
</dt> <dt>

[Exemplos de classe auxiliar NDF](ndf-helper-class-examples.md)
</dt> </dl>

 

