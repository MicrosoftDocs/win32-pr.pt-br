---
description: A DEP (prevenção de execução de dados) é um recurso de proteção de memória no nível do sistema que é criado no sistema operacional, começando com o Windows XP e o Windows Server 2003.
ms.assetid: 75cd83a5-4b77-4ca9-b595-e32d0dd609d0
title: Prevenção de Execução de Dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc53febb383ef2789c2798b091960c2d20856d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780621"
---
# <a name="data-execution-prevention"></a>Prevenção de Execução de Dados

A DEP (prevenção de execução de dados) é um recurso de proteção de memória no nível do sistema que é criado no sistema operacional, começando com o Windows XP e o Windows Server 2003. O DEP permite que o sistema marque uma ou mais páginas de memória como não executáveis. Marcar regiões de memória como não executáveis significa que o código não pode ser executado dessa região de memória, o que dificulta a exploração de estouros de buffer.

A DEP impede que o código seja executado a partir de páginas de dados como heap, pilhas e pools de memória padrão. Se um aplicativo tentar executar o código de uma página de dados protegida, ocorrerá uma exceção de violação de acesso à memória e, se a exceção não for tratada, o processo de chamada será encerrado.

A DEP não se destina a ser uma defesa abrangente contra todas as explorações; Ela se destina a ser outra ferramenta que você pode usar para proteger seu aplicativo.

## <a name="how-data-execution-prevention-works"></a>Como funciona a prevenção de execução de dados

Se um aplicativo tentar executar o código de uma página protegida, o aplicativo receberá uma exceção com o status **código \_ status \_ violação de acesso**. Se seu aplicativo deve executar o código de uma página de memória, ele deve alocar e definir os atributos de [proteção de memória](memory-protection.md) virtual apropriados. A memória alocada deve ser marcada como **Page \_ Execute**, **Page \_ Execute \_ Read**, **Page \_ Execute \_ ReadWrite** ou **Page \_ Execute \_ WRITECOPY** ao alocar memória. As alocações de heap feitas chamando as funções **malloc** e [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) são não executáveis.

Os aplicativos não podem executar o código do heap de processo padrão ou da pilha.

O DEP é configurado na inicialização do sistema de acordo com a configuração de política de proteção de página sem execução nos dados de configuração da inicialização. Um aplicativo pode obter a configuração de política atual chamando a função [**GetSystemDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-getsystemdeppolicy) . Dependendo da configuração de política, um aplicativo pode alterar a configuração de DEP para o processo atual chamando a função [**SetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy) .

## <a name="programming-considerations"></a>Considerações sobre programação

Um aplicativo pode usar a função do [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) para alocar memória executável com as opções de proteção de memória apropriadas. É recomendável que um conjunto de aplicativos, no mínimo, a opção de proteção de memória de **\_ execução de página** . Depois que o código executável é gerado, é recomendável que o aplicativo defina as proteções de memória para não permitir acesso de gravação à memória alocada. Os aplicativos podem não permitir o acesso de gravação à memória alocada usando a função [**usar VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) . A despermissão de acesso de gravação garante a proteção máxima para regiões executáveis do espaço de endereço do processo. Você deve tentar criar aplicativos que usam o menor espaço de endereço executável possível, o que minimiza a quantidade de memória exposta à exploração de memória.

Você também deve tentar controlar o layout da memória virtual do seu aplicativo e criar regiões executáveis. Essas regiões executáveis devem estar localizadas em um espaço de memória menor do que as regiões não executáveis. Ao localizar regiões executáveis abaixo de regiões não executáveis, você pode ajudar a evitar que um estouro de buffer flua para a área executável da memória.

## <a name="application-compatibility"></a>Compatibilidade de aplicativos

Algumas funcionalidades de aplicativos são incompatíveis com o DEP. Os aplicativos que executam geração de código dinâmico (como geração de código just-in-time) e não marcam explicitamente o código gerado com permissão de execução podem ter problemas de compatibilidade em computadores que usam o DEP. Os aplicativos escritos no Active Template Library (ATL) versão 7,1 e anteriores podem tentar executar código em páginas marcadas como não executáveis, o que dispara uma falha de NX e encerra o aplicativo; para obter mais informações, consulte [**SetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy). A maioria dos aplicativos que executa ações incompatíveis com o DEP deve ser atualizada para funcionar corretamente.

Um pequeno número de arquivos e bibliotecas executáveis pode conter código executável na seção de dados de um arquivo de imagem. Em alguns casos, os aplicativos podem posicionar pequenos segmentos de código (comumente chamados de conversões) nas seções de dados. No entanto, a DEP marca as seções do arquivo de imagem que é carregado na memória como não executável, a menos que a seção tenha o atributo executável aplicado.

Portanto, o código executável nas seções de dados deve ser migrado para uma seção de código ou a seção de dados que contém o código executável deve ser explicitamente marcada como executável. O atributo executável, **Image \_ SCN \_ mem \_ Execute**, deve ser adicionado ao campo **características** do cabeçalho da seção correspondente para as seções que contêm código executável. Para obter mais informações sobre como adicionar atributos a uma seção, consulte a documentação incluída com o vinculador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Prevenção de execução de dados (TechNet)](/previous-versions/windows/it-pro/windows-xp/bb457155(v=technet.10))
</dt> <dt>

[Como configurar a proteção de memória](https://www.microsoft.com/technet/security/prodtech/windowsxp/depcnfxp.mspx)
</dt> <dt>

[Artigo 875352 da base de conhecimento](https://support.microsoft.com/kb/875352)
</dt> </dl>

 

 
