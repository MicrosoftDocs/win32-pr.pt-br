---
description: O provedor de Windows Driver Model (WDM) concede acesso às classes, instâncias, métodos e eventos de drivers de hardware que estão em conformidade com o modelo WDM.
ms.assetid: 8686a613-0e53-4e6e-b193-7839abfb70de
ms.tgt_platform: multiple
title: Acessando dados de drivers de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a59b59116ca0f71178fb2faed290d6bc76c9d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765760"
---
# <a name="accessing-data-from-device-drivers"></a>Acessando dados de drivers de dispositivo

O provedor de Windows Driver Model (WDM) concede acesso às classes, instâncias, métodos e eventos de drivers de hardware que estão em conformidade com o modelo WDM. As classes para drivers de hardware residem no \\ \\ \\ namespace raiz WMI.

O provedor WDM é de interesse daqueles que escrevem drivers de dispositivo e administradores que estão interessados em dados de driver de dispositivo.

As seções a seguir são discutidas neste tópico:

-   [Informações para gravadores de driver de dispositivo](#information-for-device-driver-writers)
-   [Informações para administradores e usuários de dados de driver](#information-for-administrators-and-users-of-driver-data)
-   [Tópicos relacionados](#related-topics)

## <a name="information-for-device-driver-writers"></a>Informações para gravadores de driver de dispositivo

As classes WMI relacionadas a um driver de dispositivo específico são criadas quando o provedor WDM extrai o MOF binário do arquivo executável do driver de dispositivo. Isso ocorre sempre que o WMI é iniciado, um novo driver de dispositivo é instalado ou a instância do [WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) para um determinado driver é excluída. Ao verificar wmiprov. log, você pode determinar se um erro resultante de falha ocorreu durante a extração do arquivo MOF binário. Detalhes de erros de [Mofcomp](mofcomp.md) são relatados em Mofcomp. log. Para obter mais informações, consulte [arquivos de log do WMI](wmi-log-files.md). Por motivos de desempenho, o provedor WDM não gera eventos durante a criação ou exclusão de classes devido a um provedor WDM iniciando ou parando.

O provedor WDM transforma todos os dados de WNODE em informações de classe. Se for encontrado um erro ao transformar os dados de WNODE em dados de classe, eles serão relatados em wmiprov. log com o cabeçalho formatado e os bytes processados na mesma forma que um despejo de memória.

As alterações feitas nas configurações de segurança do driver não entram em vigor até que o provedor WDM seja descarregado e recarregado. Para obter mais informações, consulte [descarregando um provedor](unloading-a-provider.md).

O WMI também pode disponibilizar contadores de alto desempenho para drivers de hardware disponíveis. Para obter mais informações sobre como criar classes de alto desempenho e exibir dados no monitor do sistema Perfmon, consulte [melhorando a eficiência de um provedor de instância](improving-the-efficiency-of-an-instance-provider.md). Para obter mais informações sobre como escrever drivers de dispositivo habilitados para WMI, consulte [https://www.microsoft.com/ddk](https://msdn.microsoft.com/library/aa972908.aspx) . Para obter mais informações sobre qualificadores específicos de WDM no arquivo MOF, consulte [**qualificadores específicos para o provedor WDM**](qualifiers-specific-to-the-wdm-provider.md).

## <a name="information-for-administrators-and-users-of-driver-data"></a>Informações para administradores e usuários de dados de driver

Listar as instâncias da classe [WMIBinaryMofResource](/windows/desktop/WmiCoreProv/wmibinarymofresource) fornece uma lista dos drivers no sistema e informações sobre se o provedor WDM teve êxito na compilação do MOFs para cada driver. Você pode forçar o provedor a recompilar e regenerar as classes de um driver excluindo a instância de WMIBinaryMofResource que representa esse driver. Os detalhes dos erros de [Mofcomp](mofcomp.md) são relatados no Mofcomp. log.

Se o namespace WMI estiver corrompido, ele poderá ser excluído e reaberto para forçar o WDM a recriar as classes de driver. Para obter mais informações sobre como abrir um namespace, consulte [Criando hierarquias dentro do WMI](creating-hierarchies-within-wmi.md).

As classes de driver podem ocasionalmente ser "retidos" se o carregamento do driver for interrompido ou se outras operações anormais ocorrerem. O provedor WDM pesquisará e limpará as classes "com falha" quando um novo driver for instalado ou quando o valor da chave do registro do **software \\ Microsoft \\ WBEM \\ WDMProvider** **ProcessStrandedClasses** for definido como **true**. Definir esse valor como **true** retarda o desempenho de inicialização do WMI devido à operação de limpeza. O valor padrão é **false**. O provedor WDM verifica apenas esse valor de registro quando o namespace "root \\ WMI" é aberto pela primeira vez.

Se forem feitas alterações de segurança em um driver de dispositivo WDM, as alterações não entrarão em vigor até que o provedor WDM seja descarregado e recarregado. O serviço de gerenciamento do Windows deve ser interrompido e reiniciado para fazer isso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o WMI](using-wmi.md)
</dt> </dl>

 

 
