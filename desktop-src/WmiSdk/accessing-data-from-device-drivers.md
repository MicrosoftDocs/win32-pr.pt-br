---
description: O Windows WDM (modelo de driver) concede acesso às classes, instâncias, métodos e eventos de drivers de hardware que estão em conformidade com o modelo do WDM.
ms.assetid: 8686a613-0e53-4e6e-b193-7839abfb70de
ms.tgt_platform: multiple
title: Acessando dados de drivers de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82bec478f83ddbc6d58419710fb868ddd233f820a06004210c1dac495de86b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131909"
---
# <a name="accessing-data-from-device-drivers"></a>Acessando dados de drivers de dispositivo

O Windows WDM (modelo de driver) concede acesso às classes, instâncias, métodos e eventos de drivers de hardware que estão em conformidade com o modelo do WDM. As classes para drivers de hardware residem no \\ \\ \\ namespace wmi raiz.

O provedor WDM é de interesse para aqueles que escrevem drivers de dispositivo e para administradores interessados em dados de driver de dispositivo.

As seções a seguir são discutidas neste tópico:

-   [Informações para autores de driver de dispositivo](#information-for-device-driver-writers)
-   [Informações para administradores e usuários de dados de driver](#information-for-administrators-and-users-of-driver-data)
-   [Tópicos relacionados](#related-topics)

## <a name="information-for-device-driver-writers"></a>Informações para autores de driver de dispositivo

As classes WMI relacionadas a um driver de dispositivo específico são criadas quando o provedor WDM extrai o MOF binário do arquivo executável do driver de dispositivo. Isso ocorre sempre que o WMI é iniciado, um novo driver de dispositivo é instalado ou a instância [de WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) para um driver específico é excluída. Ao verificar Wmiprov.log, você pode determinar se ocorreu um erro resultando em falha ao extrair o arquivo MOF binário. Detalhes de [erros mofcomp](mofcomp.md) são relatados em Mofcomp.log. Para obter mais informações, consulte [Arquivos de log WMI](wmi-log-files.md). Por motivos de desempenho, o provedor WDM não gera eventos durante a criação ou exclusão de classes devido a um provedor WDM iniciar ou parar.

O provedor WDM transforma todos os dados WNODE em informações de classe. Se um erro for encontrado ao transformar os dados do WNODE em dados de classe, eles serão relatados em Wmiprov.log com o título formatado e bytes renderizados na mesma forma que um despejo de memória.

As alterações feitas nas configurações de segurança do driver não são efetivadas até que o provedor WDM seja descarregado e recarregado. Para obter mais informações, [consulte Descarregando um provedor](unloading-a-provider.md).

O WMI também pode disponibilizar contadores de alto desempenho para drivers de hardware. Para obter mais informações sobre como criar classes de alto desempenho e exibir dados no Monitor do Sistema Perfmon, consulte Melhorando a eficiência [de um provedor de instância.](improving-the-efficiency-of-an-instance-provider.md) Para obter mais informações sobre como escrever drivers de dispositivo habilitados para WMI, consulte [https://www.microsoft.com/ddk](https://msdn.microsoft.com/library/aa972908.aspx) . Para obter mais informações sobre qualificadores específicos do WDM no arquivo MOF, consulte [**Qualificadores específicos para o provedor WDM.**](qualifiers-specific-to-the-wdm-provider.md)

## <a name="information-for-administrators-and-users-of-driver-data"></a>Informações para administradores e usuários de dados de driver

Listar as instâncias da classe [WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) fornece uma lista dos drivers no sistema e informações sobre se o provedor WDM teve êxito na compilação dos MOFs para cada driver. Você pode forçar o provedor a recompilar e regenerar as classes de um driver excluindo a instância de WMIBinaryMofResource que representa esse driver. Os detalhes [dos erros mofcomp](mofcomp.md) são relatados no Mofcomp.log.

Se o namespace WMI estiver corrompido, ele poderá ser excluído e reaberto para forçar o WDM a recriar as classes de driver. Para obter mais informações sobre como abrir um namespace, consulte [Criando hierarquias no WMI](creating-hierarchies-within-wmi.md).

Às vezes, as classes de driver podem ficar "desnorteadas" se o carregamento do driver for interrompido ou outras operações anormais ocorrerem. O provedor WDM só pesquisa e limpa classes "encadeadas" quando um novo driver é instalado ou quando o valor da chave do Registro **ProcessStrandedClasses** do **\\ \\ WBEM \\** do Microsoft Software está definido como **TRUE.** Definir esse valor como **TRUE** reduz o desempenho de inicialização do WMI devido à operação de limpeza. O valor padrão é **FALSE**. O provedor WDM verifica apenas esse valor do Registro quando o \\ namespace "Wmi raiz" é aberto pela primeira vez.

Se alterações de segurança são feitas em um driver de dispositivo WDM, as alterações não entrarão em vigor até que o provedor WDM seja descarregado e recarregado. O Windows gerenciamento de dados deve ser interrompido e reiniciado para fazer isso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o WMI](using-wmi.md)
</dt> </dl>

 

 
