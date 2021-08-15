---
title: Servidor de Política de Rede & Serviço de Autenticação da Internet
description: Saiba mais sobre o Serviço de Autenticação da Internet e o Servidor de Políticas de Rede. O IAS (Serviço de Autenticação da Internet) foi renomeado como NPS (Servidor de Políticas de Rede).
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f46e4052b2c7277f49f898a290d689928b5838c0562042c0ba8937c5daf00210
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118362312"
---
# <a name="internet-authentication-service--network-policy-server"></a>Servidor de Política de Rede & Serviço de Autenticação da Internet

O IAS (Serviço de Autenticação da Internet) foi renomeado como NPS (Servidor de Políticas de Rede).

## <a name="internet-authentication-service"></a>Serviço de autenticação da Internet

O Serviço de Autenticação da Internet é a implementação da Microsoft de um servidor RADIUS e proxy.

O Serviço de Autenticação da Internet dá suporte a dois conjuntos de API: API de Extensões do Servidor de Política [de Rede](ias-extensions.md) e API de Objetos de Dados [do Servidor](server-data-objects.md).

Confira [TechNet: Serviço de Autenticação da Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) para obter mais informações sobre a IAS.

## <a name="network-policy-server"></a>Servidor de Políticas de Rede

O Servidor de Política de Rede é a implementação da Microsoft de um servidor RADIUS e proxy e está disponível em servidores Windows a partir do Windows Server 2008.

O NPS dá suporte aos mesmos dois conjuntos de API que o IAS: API de Extensões do Servidor de Política de [Rede](ias-extensions.md) e [API de Objetos de Dados do Servidor](server-data-objects.md).

Além disso, o NPS contém um conjunto de novos recursos que expandem os recursos de IAS.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Recurso</th>
<th>Novidades do NPS</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/NAP/network-access-protection-start-page">NAP (Proteção de Acesso à Rede)</a><br/></td>
<td>O NPS é o servidor central da Proteção de Acesso à Rede.<br/> O NPS dá suporte à geração de políticas usando as seguintes condições adicionais:<br/>
<ul>
<li>Expiração da política.</li>
<li>Versão do sistema operacional.</li>
<li>Acessar o endereço IP do cliente.</li>
<li>Políticas de saúde.</li>
<li>Tipos de EAP permitidos.</li>
<li>Hcap.</li>
</ul>
O NPS dá suporte à criação de políticas usando as seguintes configurações adicionais:<br/>
<ul>
<li>Condicional.</li>
<li>Acesso limitado.</li>
<li>Estado estendido para acesso limitado.</li>
</ul>
O NPS, por meio de NAP, interopera com o CISCO NAC.<br/> A IAS não dá suporte a NAP.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/eap/eap-start-page">EAP</a> Suporte a <a href="/windows/win32/eaphost/portal">Política e EAPHost</a><br/></td>
<td>O NPS usa EAPHost para extensibilidade de método EAP. Além disso, os administradores podem configurar a política de acesso à rede para EAP.<br/> A IAS não dá suporte à integração de EAPHost ou às condições de filtro de tipo EAP para políticas.<br/></td>
</tr>
<tr class="odd">
<td>Suporte a IPv6<br/></td>
<td>O NPS dá suporte à implantação em ambientes IPv6.<br/> A IAS não dá suporte a endereços de rede IPv6.<br/></td>
</tr>
<tr class="even">
<td>Configuração de XML<br/></td>
<td>A configuração do NPS pode ser importada e exportada no formato XML.<br/> A IAS está usando um banco de dados Jet para armazenar a configuração do serviço.<br/></td>
</tr>
<tr class="odd">
<td><a href="https://www.niap-ccevs.org/cc-scheme/">Critérios comuns</a> Apoio<br/></td>
<td>O NPS foi atualizado para dar suporte à sua implantação em ambientes que devem atender aos padrões de segurança de Critérios Comuns.<br/></td>
</tr>
<tr class="even">
<td><a href="ias-extensions.md">API de Extensões do NPS</a><br/></td>
<td>As DLLs de extensão NPS são executados em um processo separado do serviço NPS. Se uma DLL de extensão falhar, o NPS continuará em execução e as solicitações futuras serão rejeitadas.<br/> As DLLs de extensão de IAS são executados no mesmo processo que o serviço IAS e podem afetar negativamente o serviço.<br/></td>
</tr>
<tr class="odd">
<td>Gerenciamento Interface do Usuário<br/></td>
<td>O console de gerenciamento npS (nps.msc) tem uma nova aparência, uma usabilidade aprimorada e abrange todas as novas funcionalidades adicionadas ao NPS.<br/> A IAS usa o console de gerenciamento ias.msc.<br/></td>
</tr>
<tr class="even">
<td>Ferramenta de Gerenciamento de Funções e Gerenciador do Servidor Integração<br/></td>
<td>O NPS é integrado ao Gerenciador do Servidor e à Ferramenta de Gerenciamento de Função. Essa integração facilita a configuração e o gerenciamento do NPS e cenários relacionados.<br/> Gerenciador do Servidor está disponível em computadores que executam a IAS.<br/></td>
</tr>
<tr class="odd">
<td>Script de linha de comando atualizado com <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">Netsh</a>.<br/></td>
<td>O NPS dá suporte à &quot; interface de linha de comando Netsh nps. &quot; &quot;O Netsh nps &quot; contém novos comandos que permitem configurar totalmente o NPS, incluindo recursos NAP.<br/> O IAS dá suporte à interface de linha de comando &quot; Netsh aaaa. &quot;<br/></td>
</tr>
<tr class="even">
<td>Isolamento de política<br/></td>
<td>O NPS permite a implementação do isolamento de política definindo a Fonte de Política de Rede. As políticas podem ser configuradas aplicável somente a um tipo de NAS predeterminado.<br/> A IAS não dá suporte ao isolamento de política.<br/></td>
</tr>
</tbody>
</table>



 

Consulte [TechNet: Servidor de Políticas de Rede](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) para obter mais informações sobre o NPS.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Autenticação RADIUS, autorização e contabilidade](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Registro em log com o servidor de políticas de rede](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[Trabalhando com um servidor de estado](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

