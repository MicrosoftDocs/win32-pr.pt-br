---
title: Serviço de autenticação da Internet & servidor de políticas de rede
description: Saiba mais sobre o serviço de autenticação da Internet e o servidor de políticas de rede. O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede).
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd62a50021c485c7bf51cdc9caff4360e4cc863
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989421"
---
# <a name="internet-authentication-service--network-policy-server"></a>Serviço de autenticação da Internet & servidor de políticas de rede

O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede).

## <a name="internet-authentication-service"></a>Serviço de autenticação da Internet

O serviço de autenticação da Internet é a implementação da Microsoft de um servidor RADIUS e proxy.

O serviço de autenticação da Internet dá suporte a dois conjuntos de API: API [das extensões do servidor de políticas de rede](ias-extensions.md) e [do Server Data Objects](server-data-objects.md).

Consulte [TechNet: serviço de autenticação da Internet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) para obter mais informações sobre o ias.

## <a name="network-policy-server"></a>Servidor de Políticas de Rede

O servidor de políticas de rede é a implementação da Microsoft de um servidor RADIUS e proxy e está disponível em servidores Windows a partir do Windows Server 2008.

O NPS dá suporte aos mesmos dois conjuntos de API que o IAS: API de [extensões do servidor de políticas de rede](ias-extensions.md) e a diretiva de [objetos de dados do servidor](server-data-objects.md)

Além disso, o NPS contém um conjunto de novos recursos que expandem os recursos do IAS.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Recurso</th>
<th>O que há de novo para o NPS</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/NAP/network-access-protection-start-page">NAP (proteção de acesso à rede)</a><br/></td>
<td>O NPS é o servidor central de proteção de acesso à rede.<br/> O NPS dá suporte à criação de política usando as seguintes condições adicionais:<br/>
<ul>
<li>Expiração da política.</li>
<li>Versão do sistema operacional.</li>
<li>Acessar o endereço IP do cliente.</li>
<li>Políticas de integridade.</li>
<li>Tipos de EAP permitidos.</li>
<li>HCAP.</li>
</ul>
O NPS dá suporte à criação de política usando as seguintes configurações adicionais:<br/>
<ul>
<li>Experiência.</li>
<li>Acesso limitado.</li>
<li>Estado estendido para acesso limitado.</li>
</ul>
O NPS, por meio de NAP, interopera com o CISCO NAC.<br/> O IAS não oferece suporte a NAP.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/eap/eap-start-page">EAP</a> Suporte a políticas e <a href="/windows/win32/eaphost/portal">EAPHost</a><br/></td>
<td>O NPS usa o EAPHost para a extensibilidade do método EAP. Além disso, os administradores podem configurar a política de acesso à rede para o EAP.<br/> O IAS não oferece suporte à integração do EAPHost ou condições de filtro de tipo EAP para políticas.<br/></td>
</tr>
<tr class="odd">
<td>Suporte a IPv6<br/></td>
<td>O NPS dá suporte à implantação em ambientes IPv6.<br/> O IAS não oferece suporte a endereços de rede IPv6.<br/></td>
</tr>
<tr class="even">
<td>Configuração de XML<br/></td>
<td>A configuração do NPS pode ser importada e exportada em formato XML.<br/> O IAS está usando um banco de dados Jet para armazenar a configuração do serviço.<br/></td>
</tr>
<tr class="odd">
<td><a href="https://www.niap-ccevs.org/cc-scheme/">Critérios comuns</a> Support<br/></td>
<td>O NPS foi atualizado para dar suporte à sua implantação em ambientes que devem atender aos padrões de segurança de critérios comuns.<br/></td>
</tr>
<tr class="even">
<td><a href="ias-extensions.md">API de extensões do NPS</a><br/></td>
<td>As DLLs de extensão do NPS são executadas em um processo separado do serviço NPS. Se uma DLL de extensão falhar, o NPS continuará em execução e as solicitações futuras serão rejeitadas.<br/> As DLLs de extensão do IAS são executadas no mesmo processo que o serviço IAS e podem afetar negativamente o serviço.<br/></td>
</tr>
<tr class="odd">
<td>Interface do usuário de gerenciamento<br/></td>
<td>O console de gerenciamento do NPS (NPS. msc) tem uma nova aparência, melhor usabilidade e abrange toda a nova funcionalidade adicionada ao NPS.<br/> O IAS usa o console de gerenciamento do IAS. msc.<br/></td>
</tr>
<tr class="even">
<td>Ferramenta de gerenciamento de função e integração de Gerenciador do Servidor<br/></td>
<td>O NPS é integrado com o Gerenciador do Servidor e a ferramenta de gerenciamento de função. Essa integração facilita a configuração e o gerenciamento do NPS e dos cenários relacionados.<br/> O Gerenciador do Servidor não está disponível em computadores que executam o IAS.<br/></td>
</tr>
<tr class="odd">
<td>Script de linha de comando atualizado com <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">netsh</a>.<br/></td>
<td>O NPS dá suporte à &quot; interface de linha de comando netsh nps &quot; . &quot;O netsh nps &quot; contém novos comandos que permitem configurar completamente o NPS, incluindo recursos NAP.<br/> O IAS dá suporte à &quot; interface de linha de comando netsh aaaa &quot; .<br/></td>
</tr>
<tr class="even">
<td>Isolamento de política<br/></td>
<td>O NPS permite a implementação do isolamento de política definindo a origem da política de rede. As políticas podem ser configuradas que são aplicáveis apenas a um tipo de NAS predeterminado.<br/> O IAS não dá suporte ao isolamento de política.<br/></td>
</tr>
</tbody>
</table>



 

Consulte [TechNet: servidor de políticas de rede](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) para obter mais informações sobre o NPS.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Autenticação, autorização e contabilização RADIUS](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Registrando em log com o servidor de políticas de rede](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[Trabalhando com um servidor de estado](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

