---
title: API WFP
description: A API da WFP (Windows Filtering Platform) é dividida nos componentes a seguir.
ms.assetid: ff3f0d74-7e0b-4a3e-b66d-eaa61b89038a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4230c82105f85c36e6fb112508a7128758b2ad60
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "105810376"
---
# <a name="wfp-api"></a>API WFP

A API da WFP (Windows Filtering Platform) é dividida nos componentes a seguir.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Componente</th>
<th>Descrição</th>
<th>Arquivos de cabeçalho</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><a href="/windows-hardware/drivers/ddi/_netvista/">API de texto explicativo</a> (FWPS) $ {remove} $<br />
</td>
<td><a href="/windows-hardware/drivers/ddi/_netvista/">Tipos de dados</a> usados por textos explicativos. <strong>Observação</strong>  Esses tipos de dados estão documentados no Microsoft Windows Driver Development Kit (DDK).<br/></td>
<td><dl> fwpstypes. h<br />
fwpstypes. idl<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="/windows-hardware/drivers/ddi/_netvista/">Funções</a> e <a href="/windows-hardware/drivers/ddi/_netvista/">tipos enumerados</a> usados para implementar textos explicativos. <strong>Observação</strong>  Essas funções e os tipos enumerados são documentados no DDK.<br/></td>
<td><dl> fwpsu. h<br />
fwpsk. h<br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2">API IKE/AuthIP (IKEEXT) $ {REMOVE} $<br />
</td>
<td><a href="fwp-enums.md">Tipos enumerados</a> e <a href="fwp-structs.md">estruturas</a> usadas para gerenciar a política e as associações de segurança do modo principal (mm) Ike e AuthIP.</td>
<td><dl> iketypes. h<br />
iketypes. idl<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="fwp-ike-functions.md">Funções</a> usadas para gerenciar a política e associações de segurança IKE e AuthIP mm.</td>
<td><dl> fwpmu. h<br />
fwpmk. h<br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2">API IPsec (IPSEC) $ {REMOVE} $<br />
</td>
<td><a href="fwp-enums.md">Tipos enumerados</a> e <a href="fwp-structs.md">estruturas</a> usadas para gerenciar diretivas IPSec e associações de segurança.</td>
<td><dl> ipsectypes. h<br />
ipsectypes. idl<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="fwp-ipsec-functions.md">Funções</a> usadas para gerenciar diretivas IPSec e associações de segurança.</td>
<td><dl> fwpmu. h<br />
fwpmk. h<br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2">API de gerenciamento (FWPM) $ {REMOVE} $<br />
</td>
<td><a href="fwp-enums.md">Tipos enumerados</a> e <a href="fwp-structs.md">estruturas</a> usadas para gerenciar o mecanismo de filtro.</td>
<td><dl> fwpmtypes. h<br />
fwpmtypes. idl<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="fwp-mgmt-functions.md">Funções</a> usadas para gerenciar o mecanismo de filtro. Essas funções são usadas para executar as seguintes tarefas:<br/>
<ul>
<li>Definir e consultar filtros, provedores e textos explicativos.</li>
<li>Recuperar estatísticas de IPsec.</li>
<li>Configure a plataforma de filtragem do Windows.</li>
</ul></td>
<td><dl> fwpmu. h<br />
fwpmk. h<br />
</dl></td>

</tr>
<tr class="odd">
<td>API compartilhada (FWP)</td>
<td><a href="fwp-enums.md">Tipos enumerados</a> fundamentais e <a href="fwp-structs.md">estruturas</a> compartilhadas na plataforma de filtragem do Windows.</td>
<td><dl> fwptypes. h<br />
fwptypes. idl<br />
</dl></td>
</tr>
</tbody>
</table>



 

Os nomes de tipos de dados são todos delimitados por letras maiúsculas e sublinhados. O nome sempre começa com um prefixo que identifica seu grupo de componentes, como [**FWPM \_ PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).

Os nomes de função são de caso misto e delimitados por maiúsculas e minúsculas. O nome sempre começa com um prefixo que identifica seu grupo de componentes, como [**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0).

A maioria dos nomes de função e de dados termina com um número de versão. O arquivo de cabeçalho fwpvi. h mapeia os dados independentes de versão e os nomes de função para a versão apropriada para uso com um determinado sistema operacional. Para obter mais informações, consulte [nomes de Version-Independent WFP e direcionamento de versões específicas do Windows](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md).

Cada componente não é autônomo. Por exemplo, as políticas de modo principal (MM) IKE são definidas no componente IKEEXT, mas são armazenadas em um contexto de provedor e são associadas a um filtro que são encontrados no componente de API FWPM.

## <a name="user-mode-and-kernel-mode-public-header-files"></a>User-Mode e Kernel-Mode arquivos de cabeçalho público

A maioria das funções de WFP pode ser chamada no modo de usuário ou no modo kernel. No entanto, as funções de modo de usuário retornam um valor **DWORD** que representa um código de erro Win32, enquanto as funções de modo kernel retornam um valor **NTSTATUS** que representa um código de status NT. Como resultado, os nomes de função e a semântica são idênticos entre o modo de usuário e o modo kernel, mas as assinaturas de função não são. Isso requer cabeçalhos específicos de modo de usuário e de modo kernel para os protótipos de função. Os nomes de arquivo de cabeçalho do modo de usuário terminam em "u" e os nomes de arquivo de cabeçalho do modo kernel terminam em "k".

A tabela a seguir lista os arquivos de cabeçalho do Win32 que definem as funções de WFP.

| Arquivos de cabeçalho | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fwpmk. h      | Protótipos de função em modo kernel para componentes FWPM, IPsec e IKEEXT. Disponível somente no DDK.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| fwpmu. h      | Protótipos de função de modo de usuário para componentes FWPM, IPsec e IKEEXT. Disponível apenas no Microsoft Windows Software Development Kit (SDK).                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| fwpsk. h      | Protótipos de função no modo kernel e tipos enumerados para o componente FWPS. Disponível somente no DDK.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| fwpsu. h      | Protótipos de função de modo de usuário e tipos enumerados para o componente FWPS. Disponível somente no SDK do Windows. **Observação**  Os tipos enumerados do modo de usuário FWPS são idênticos aos tipos enumerados do modo kernel FWPS. Em consequência, esses tipos são documentados apenas no DDK.<br/> **Observação**  Os protótipos de função FWPS de modo de usuário são idênticos aos protótipos de função FWPS de modo kernel com a exceção do código de retorno. As funções FWPS de modo de usuário retornam uma **DWORD**, enquanto as funções FWPS de modo kernel retornam um **NTSTATUS**. Em consequência, essas funções são documentadas somente no DDK.<br/> |



 

Todas as funções de modo de usuário são exportadas de fwpuclnt.dll. Todas as funções de modo kernel são exportadas de fwpkclnt.sys.

### <a name="management-fwpm-and-callout-fwps-data-types"></a>Tipos de dados de gerenciamento (FWPM) e texto explicativo (FWPS)

A maioria dos tipos de dados FWPM, que são usados para tarefas de gerenciamento, como adicionar filtros ou textos explicativos de um aplicativo ou driver, têm contrapartes FWPS. Os tipos de dados FWPS são usados durante a filtragem real do tráfego de rede, no contexto de uma rotina de texto explicativo para classificação.

Por exemplo, para adicionar um filtro a uma determinada camada de mecanismo de filtragem, o programador deve usar um tipo FWPM, como: `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET` . Para verificar a qual camada um texto explicativo está sendo chamado, o programador deve usar o tipo de FWPS correspondente: ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)` .

Algumas contrapartes FWPS para tipos de dados FWPM estão expandindo os tipos de dados FWPM originais. Por exemplo, para adicionar uma condição de filtro em muitas camadas de mecanismo de filtragem, o programador especifica o mesmo que a `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` camada do mecanismo de filtragem. Para localizar um valor de condição de filtro, o programador especifica um tipo de FWPS específico de camada, como: `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]` .

Os tipos de dados FWPS são geralmente menores do que suas contrapartes FWPM. Por exemplo, os [**identificadores da camada de filtragem FWPM**](management-filtering-layer-identifiers-.md) são **GUIDs**(16 bytes) enquanto os [identificadores da camada de filtragem FWPS](/windows-hardware/drivers/network/management-filtering-layer-identifiers) são **UINT16** (16 bits). O tamanho menor para os tipos de dados FWPS melhora o desempenho do sistema, pois comparações de inteiros compensam as comparações de **GUID** para tráfego em tempo real. Além disso, a memória do kernel é usada com eficiência, pois os tipos FWPS são todos usados no kernel para gerenciar os filtros, enquanto os tipos FWPM são armazenados no modo de usuário para gerenciar as diferentes camadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelo de objeto da API WFP](object-model.md)
</dt> <dt>

[Gerenciamento de objetos de API WFP](object-management.md)
</dt> </dl>

