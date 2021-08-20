---
title: Usar o DRED para diagnosticar falhas de GPU
description: O dispositivo removeu dados estendidos (DRED com) é um conjunto crescente de recursos de diagnóstico projetados para ajudá-lo a identificar a causa de erros inesperados de remoção do dispositivo.
ms.custom: 19H1
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: ecb18b81107123564e265e49fad61c004b17938f732b373311743bf64bd92fab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118097640"
---
# <a name="use-dred-to-diagnose-gpu-faults"></a>Usar o DRED para diagnosticar falhas de GPU
DRED com significa dados estendidos removidos do dispositivo. DRED com é um conjunto em evolução de recursos de diagnóstico projetados para ajudá-lo a identificar a causa de erros inesperados de remoção de dispositivo. Em hardware que dá suporte aos recursos necessários (conforme definido abaixo), o DRED com fornece trilhas automáticas, bem como o relatório de falhas de página da GPU.

## <a name="auto-breadcrumbs"></a>Trilhas automáticas
Para definir a cena para as trilhas automáticas, vamos primeiro mencionar a variedade manual. Ao prever a eventualidade de uma [TdR (detecção de tempo limite e recuperação)](/windows-hardware/drivers/display/timeout-detection-and-recovery), você pode usar o [método ID3D12GraphicsCommandList2:: WriteBufferImmediate](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate) para posicionar as *trilhas* no fluxo de comando da GPU, a fim de acompanhar o progresso da GPU.

Essa é uma abordagem razoável se você quiser criar uma implementação personalizada e de baixa sobrecarga. mas pode não ter alguma versatilidade de uma solução padronizada, como extensões do depurador ou relatórios via [Relatório de Erros do Windows (WER)](/windows/desktop/wer/windows-error-reporting) (também conhecido como Watson).

Portanto, as trilhas automáticas do DRED com chamam **WriteBufferImmediate** para posicionar os contadores de progresso no fluxo do comando da GPU. DRED com insere um breadcrumb após cada *op de renderização*, &mdash; o que significa todas as operações que resultam em trabalho de GPU (por exemplo, **empate**, **expedição**, **cópia**, **resolução** e outros). Se o dispositivo for removido no meio de uma carga de trabalho de GPU, o valor de trilha de DRED com será essencialmente uma coleção de operações de renderização concluídas antes do erro.

O buffer de anéis do histórico de navegação estrutural retém até operações 64KiB em uma determinada lista de comandos. Se houver mais de 65536 operações em uma lista de comandos, somente as últimas operações de 64KiB serão armazenadas &mdash; substituindo primeiro as operações mais antigas. No entanto, o valor do contador de navegação estrutural continua a contagem até `UINT_MAX` . Portanto, LastOpIndex = (BreadcrumbCount-1) %65536.

o dred com 1,0 foi disponibilizado pela primeira vez em Windows 10, versão 1809 (Atualização de outubro de 2018 para o Windows 10), e ele expôs trilhas de autoria. No entanto, não havia nenhuma API para ela, e a única maneira de habilitar o Dred com 1,0 era usar o **Hub de comentários** para capturar uma reprodução de TDR (reprodução) para **aplicativos & jogos** de \> **desempenho e compatibilidade do jogo**. A principal finalidade do DRED com 1,0 foi ajudar a gerar falhas do jogo por meio de comentários do cliente.
### <a name="caveats"></a>Advertências
- Como uma GPU é muito pipeline, não há garantia de que o contador de navegação estrutural indica a operação exata que falhou. Na verdade, em alguns dispositivos de renderização adiados baseados em bloco, é possível que o contador de navegação estrutural seja um recurso completo ou uma barreira de UAV (exibição de acesso não ordenado) por trás do andamento real da GPU.
- Um driver de vídeo pode reordenar comandos, buscar previamente a memória do recurso antes de executar um comando ou liberar a memória armazenada em cache bem após a conclusão de um comando. Qualquer um deles pode produzir um erro de GPU. Nesses casos, os contadores de Breadcrumbs automáticos podem ser menos úteis ou enganosos.
### <a name="performance"></a>Desempenho
Embora as trilhas automáticas sejam projetadas para serem de baixa sobrecarga, elas não são gratuitas. As medições de empírica mostram 2-5% de perda de desempenho em um mecanismo típico de jogos de gráficos AAA Direct3D 12. Por esse motivo, as trilhas automáticas estão desativadas por padrão.
### <a name="hardware-requirements"></a>Requisitos de hardware
Como os valores do contador de navegação estrutural devem ser preservados após a remoção do dispositivo, o recurso que contém as trilhas deve existir na memória do sistema e deve persistir no caso de remoção do dispositivo. Isso significa que o driver de vídeo precisa dar suporte a [**D3D12_FEATURE_EXISTING_HEAPS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature). felizmente, esse é o caso para a maioria dos drivers de exibição do Direct3D 12 em Windows 10, versão 1903.
## <a name="gpu-page-fault-reporting"></a>Relatório de falhas de página de GPU
Um recurso novo para DRED com 1,1 é o relatório de falhas de página de GPU DRED com. Uma falha de página de GPU geralmente ocorre em uma dessas condições.

1. Um aplicativo executa erroneamente o trabalho na GPU que faz referência a um objeto excluído. Essa é uma das principais razões para uma remoção inesperada do dispositivo.
2. Um aplicativo executa erroneamente o trabalho na GPU que acessa um recurso removido, ou um bloco não residente.
3. Um sombreador faz referência a um descritor não inicializado ou obsoleto.
3. Um sombreador indexa além do fim de uma associação de raiz.

O DRED com tenta abordar alguns desses cenários, relatando os nomes e os tipos de quaisquer objetos de API existentes ou recentemente liberados que correspondam ao endereço virtual (VA) da falha de página relatada pela GPU.

### <a name="caveat"></a>ADVERTÊNCIA
Nem todas as GPUs dão suporte a falhas de página (embora muitas delas). Algumas GPUs respondem a falhas de memória de: gravações de bit-Bucket; lendo dados simulados (por exemplo, zeros); ou simplesmente deslocando. Infelizmente, nos casos em que a GPU não trava imediatamente, uma [TdR (detecção de tempo limite e recuperação)](/windows-hardware/drivers/display/timeout-detection-and-recovery) pode ocorrer posteriormente no pipe, tornando ainda mais difícil localizar a causa raiz.

### <a name="performance"></a>Desempenho
O tempo de execução do Direct3D 12 deve organizar ativamente uma coleção de objetos de API existentes e excluídos recentemente indexáveis por VA (endereço virtual). Isso aumenta a sobrecarga de memória do sistema e apresenta um pequeno impacto de desempenho na criação e destruição de objetos. Por esse motivo, esse comportamento está desativado por padrão.

### <a name="hardware-requirements"></a>Requisitos de hardware
Uma GPU que não dá suporte à falha de página ainda pode se beneficiar do recurso de trilha automática.

## <a name="setting-up-dred-in-code"></a>Configurando o DRED com no código
As configurações de DRED com são globais para o processo e você deve configurá-las antes de criar um dispositivo Direct3D 12. Para fazer isso, chame a função [**D3D12GetDebugInterface**](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface) para recuperar um [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/desktop/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings).

```cpp
CComPtr<ID3D12DeviceRemovedExtendedDataSettings> pDredSettings;
VERIFY_SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&pDredSettings)));

// Turn on auto-breadcrumbs and page fault reporting.
pDredSettings->SetAutoBreadcrumbsEnablement(D3D12_DRED_ENABLEMENT_FORCED_ON);
pDredSettings->SetPageFaultEnablement(D3D12_DRED_ENABLEMENT_FORCED_ON);
```

> [!NOTE]
> As modificações nas configurações do DRED com não têm nenhum efeito sobre os dispositivos já criados. Mas as chamadas subsequentes para [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) usam as configurações de Dred com mais recentes.

## <a name="accessing-dred-data-in-code"></a>Acessando dados do DRED com no código
Depois que a remoção do dispositivo for detectada (por exemplo, **presente** retorna [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/com/com-error-codes-10)), use os métodos da interface [**ID3D12DeviceRemovedExtendedData**](/windows/desktop/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) para acessar os dados do Dred com para o dispositivo removido.

Para recuperar a interface **ID3D12DeviceRemovedExtendedData** , chame [QueryInterface](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void)) em uma interface [ID3D12Device](/windows/win32/api/d3d12/nn-d3d12-id3d12device) (ou derivada), passando o identificador de interface (IID) de **ID3D12DeviceRemovedExtendedData**.

```cpp
void MyDeviceRemovedHandler(ID3D12Device * pDevice)
{
    CComPtr<ID3D12DeviceRemovedExtendedData> pDred;
    VERIFY_SUCCEEDED(pDevice->QueryInterface(IID_PPV_ARGS(&pDred)));
    D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT DredAutoBreadcrumbsOutput;
    D3D12_DRED_PAGE_FAULT_OUTPUT DredPageFaultOutput;
    VERIFY_SUCCEEDED(pDred->GetAutoBreadcrumbsOutput(&DredAutoBreadcrumbsOutput));
    VERIFY_SUCCEEDED(pDred->GetPageFaultAllocationOutput(&DredPageFaultOutput));
    // Custom processing of DRED data can be done here.
    // Produce telemetry...
    // Log information to console...
    // break into a debugger...
}
```

## <a name="debugger-access-to-dred"></a>Acesso do depurador ao DRED com
Os depuradores têm acesso aos dados do DRED com por meio do **d3d12!** Exportação de dados do D3D12DeviceRemovedExtendedData.

## <a name="dred-telemetry"></a>Telemetria DRED com
Seu aplicativo pode usar as APIs DRED com para controlar os recursos do DRED com e coletar telemetria para ajudar a analisar problemas. Isso lhe dá uma rede muito mais ampla para capturar as TDRs de difícil reprodução.

a partir do Windows 10, a versão 1903, todos os eventos removidos do dispositivo no modo de usuário são relatados para [Relatório de Erros do Windows (WER)](/windows/desktop/wer/windows-error-reporting), também conhecido como Watson. Se uma combinação específica de aplicativo, GPU e driver de vídeo gerar um número suficiente de eventos removidos do dispositivo, será possível que o DRED com seja temporariamente habilitado para clientes que iniciam o mesmo aplicativo em uma configuração semelhante.
