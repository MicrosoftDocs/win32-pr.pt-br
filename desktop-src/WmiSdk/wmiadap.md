---
description: Wmiadap é um aplicativo que é executado no Windows que pode atualizar informações de desempenho no repositório do WMI.
ms.assetid: 459fe19e-3e2e-4a58-b3e7-75fd285f7389
ms.tgt_platform: multiple
title: Wmiadap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa5d2de65e8566283b341c5af52048cc79cc0299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171960"
---
# <a name="wmiadap"></a>Wmiadap

Wmiadap é um aplicativo que é executado no Windows que pode atualizar informações de desempenho no repositório do WMI. Em geral, isso permite que os desenvolvedores e os administradores de ti criem scripts que acessam informações de desempenho, como a quantidade de memória usada por um aplicativo. O tópico a seguir descreve a interface de linha de comando que você pode usar para controlar como o WMIAdap recupera informações.

O WMIAdap é instalado com o sistema operacional na maioria dos sistemas, no diretório C: \\ Windows \\ System32 \\ WBEM. Se você estiver vendo mensagens de erro relativas a wmiadap.exe, pesquise [suporte da Microsoft](https://support.microsoft.com/). Em geral, você não deve excluir wmiadap.exe do seu sistema, a menos que seja instruído de outra forma.

A transferência de dados das bibliotecas de desempenho e a atualização de classes derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) é feita pelos provedores [WmiPerfClass](wmi-providers.md) e [WMIPerfInst](wmi-providers.md) . O provedor WmiPerfClass atualiza as [classes do contador de desempenho](/windows/desktop/CIMWin32Prov/performance-counter-classes) WMI somente quando um novo objeto de desempenho é adicionado. Você ainda pode executar o WMIAdap com a opção **/r** para analisar os drivers de Windows Driver Model para criar objetos de desempenho. A opção **/f** ainda força uma atualização das classes WMI das bibliotecas de desempenho.

As opções a seguir estão disponíveis no prompt de comando.

**WMIAdap** \[  \] /f \[ **/r**\]

## <a name="switches"></a>Comutadores

<dl> <dt>

<span id="_f"></span><span id="_F"></span>**f**
</dt> <dd>

Analisa todas as bibliotecas de desempenho no sistema e atualiza as classes derivadas de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) e [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Analisa todos os drivers de Windows Driver Model no sistema para criar objetos de desempenho.

</dd> </dl>

## <a name="see-also"></a>Confira também

<dl> <dt>

[Bibliotecas de desempenho e WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[**winmgmt**](winmgmt.md)
</dt> </dl>

 

 
