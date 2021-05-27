---
title: Caixas de diálogo abrir e salvar como
description: A caixa de diálogo abrir permite que o usuário especifique a unidade, o diretório e o nome de um arquivo ou conjunto de arquivos a ser aberto.
ms.assetid: 5676ca9d-daca-40bf-8881-def2ff841c58
keywords:
- Biblioteca de caixa de diálogo comum
- caixas de diálogo comuns
- Abrir caixa de diálogo
- caixa de diálogo Salvar Como
- Personalizando a caixa de diálogo aberta
- Personalizando a caixa de diálogo Salvar como
- caixas de diálogo, abra
- caixas de diálogo, salvar como
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: be957276f0d5a6370bb53aca4b1af5052b422011
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548881"
---
# <a name="open-and-save-as-dialog-boxes"></a>Caixas de diálogo abrir e salvar como

> [!NOTE]
> A função [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) é demonstrada no [exemplo o arquivo está em uso](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse).

\[A partir do Windows Vista, as caixas de diálogo **abrir** e **salvar como** comuns foram substituídas pela [caixa de diálogo de item comum](../shell/common-file-dialog.md). Recomendamos que você use a API de caixa de diálogo de item comum em vez dessas caixas de diálogo da biblioteca de caixas de diálogo comuns.\]

A caixa de diálogo **abrir** permite que o usuário especifique a unidade, o diretório e o nome de um arquivo ou conjunto de arquivos a ser aberto. Você cria e exibe uma caixa de diálogo **aberta** inicializando uma estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) e passando a estrutura para a função [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) .

A caixa de diálogo **salvar como** permite que o usuário especifique a unidade, o diretório e o nome de um arquivo a ser salvo. Você cria e exibe uma caixa de diálogo **salvar como** inicializando uma estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) e passando a estrutura para a função [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) .

As caixas de diálogo **abrir** e **salvar** no estilo do Gerenciador fornecem recursos de interface do usuário que são semelhantes ao Windows Explorer. No entanto, o sistema continua a oferecer suporte a caixas de diálogo **abrir** e **salvar como** de estilo antigo para aplicativos que devem ser consistentes com a interface do usuário de estilo antigo.

Além da diferença na aparência, as caixas de diálogo estilo do Gerenciador e estilo antigo diferem no uso dos modelos personalizados e dos procedimentos de conexão para personalizar as caixas de diálogo. No entanto, as caixas de diálogo estilo Explorer e de estilo antigo têm o mesmo comportamento para a maioria das operações básicas, como especificar um filtro de nome de arquivo, validar a entrada do usuário e obter o nome de arquivo especificado pelo usuário. Para obter mais informações sobre as caixas de diálogo estilo Explorer e de estilo antigo, consulte [Abrir e salvar como personalização](#open-and-save-as-dialog-box-customization)da caixa de diálogo .

A ilustração a seguir mostra uma caixa de diálogo **Abrir** típica no estilo Explorer.

![caixa de diálogo abrir arquivo](images/opendialogboxxp.png)

A ilustração a seguir mostra uma caixa de diálogo Típica **Salvar como** no estilo Explorer.

![caixa de diálogo salvar arquivo](images/saveasdialogboxxp.png)

Se o usuário especificar um nome de arquivo e clicar **no botão OK,** [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) ou [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) **retornará TRUE.** O buffer apontado pelo membro **lpstrFile** da estrutura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) contém o caminho completo e o nome do arquivo especificados pelo usuário.

Se o usuário cancelar a **caixa de diálogo Abrir** ou Salvar **como** ou ocorrer um erro, a função retornará **FALSE.** Para determinar a causa do erro, chame a [**função CommDlgExtendedError**](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror) para recuperar o valor de erro estendido. Se o buffer **lpstrFile** for muito pequeno para receber o nome completo, **CommDlgExtendedError** retornará **FNERR \_ BUFFERTOOSMALL** e os dois primeiros bytes do buffer apontados pelo membro **lpstrFile** serão definidos como um valor inteiro especificando o tamanho necessário para receber o nome completo.

Os tópicos a seguir são discutidos nesta seção.

-   [Nomes e diretórios de arquivos](#file-names-and-directories)
-   [Filtros](#filters)
-   [Validação de arquivo e diretório](#file-and-directory-validation)
-   [Personalização da caixa de diálogo Abrir e Salvar como](#open-and-save-as-dialog-box-customization)
-   [Procedimentos de gancho no estilo explorer](#explorer-style-hook-procedures)
-   [Modelos personalizados no estilo explorer](#explorer-style-custom-templates)
-   [Identificadores de controle de estilo explorer](#explorer-style-control-identifiers)
-   [Personalização de Old-Style caixas de diálogo](#customizing-old-style-dialog-boxes)

## <a name="file-names-and-directories"></a>Nomes e diretórios de arquivos

As informações contidas nesta seção aplicam-se às caixas de diálogo do estilo do Explorer e do estilo antigo **abrir** e **salvar como** .

Antes de chamar as funções [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) ou [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) , o membro **lpstrFile** da estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) deve apontar para o buffer para receber o nome do arquivo. O membro **nMaxFile** deve especificar o tamanho, em caracteres, do buffer **lpstrFile** . Para uma função ANSI, esse é o número de bytes, mas para uma função Unicode, esse é o número de caracteres.

Se o usuário especificar um nome de arquivo e clicar no botão **OK** , a caixa de diálogo copiará a unidade, o diretório e o nome de arquivo selecionados para o buffer **lpstrFile** . A função também define os membros **nFileOffset** e **nFileExtension** com os deslocamentos, em caracteres, desde o início do buffer até o nome do arquivo e para a extensão de nome de arquivo, respectivamente.

Para recuperar apenas o nome do arquivo e a extensão, defina o membro **lpstrFileTitle** para apontar para um buffer e defina o membro **nMaxFileTitle** como o tamanho, em caracteres, do buffer. Como alternativa, você pode passar o buffer **lpstrFile** em uma chamada para a função [**GetFileTitle**](/windows/desktop/api/Commdlg/nf-commdlg-getfiletitlea) para obter o nome de exibição do arquivo selecionado. No entanto, observe que o nome do arquivo que **GetFileTitle** retornará inclui uma extensão somente se essa for a preferência do usuário para exibir nomes de arquivo.

A caixa de diálogo usa o diretório atual para o processo de chamada como o diretório inicial do qual exibir arquivos e diretórios. Use as funções [**GetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory) e [**SetCurrentDirectory**](/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory) para obter e alterar o diretório atual de um processo. Para especificar um diretório inicial diferente sem alterar o diretório atual, use o membro **lpstrInitialDir** para especificar o nome de um diretório. A caixa de diálogo altera automaticamente o diretório atual quando o usuário seleciona uma unidade ou diretório diferente. Para impedir que a caixa de diálogo altere o diretório atual, de definir **o sinalizador OFN \_ NOCHANGEDIR.** Esse sinalizador não impede que o usuário mude de diretório para encontrar um arquivo.

Para especificar uma extensão de nome de arquivo padrão, use **o membro lpstrDefExt.** Se o usuário especificar um nome de arquivo que não tem uma extensão, a caixa de diálogo adiciona sua extensão padrão. Se você especificar uma extensão padrão e o usuário especificar um nome de arquivo com uma extensão diferente, a caixa de diálogo definirá o **sinalizador OFN \_ EXTENSIONDIFFERENT.**

Para permitir que o usuário selecione mais de um arquivo de um diretório, de definir o **sinalizador OFN \_ ALLOWMULTISELECT.** Para compatibilidade com aplicativos mais antigos, a caixa de diálogo de seleção múltipla padrão usa a interface do usuário de estilo antigo. Para exibir uma caixa de diálogo seleção múltipla no estilo Explorer, você também deve definir o **sinalizador OFN \_ EXPLORER.**

Se o usuário selecionar mais de um arquivo, o buffer apontado pelo membro **lpstrFile** retornará o caminho para o diretório atual seguido pelos nomes de arquivo dos arquivos selecionados. O **membro nFileOffset** é o deslocamento para o primeiro nome de arquivo e o **membro nFileExtension** não é usado. A tabela a seguir descreve a diferença entre as caixas de diálogo estilo Explorer e de estilo antigo ao retornar vários nomes de arquivo.



| Estilo da caixa de diálogo            | Description                                                                                                                                                                                                               |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Caixas de diálogo no estilo explorer | As cadeias de caracteres de nome de arquivo e diretório são separadas por **NULL,** com um caractere **NULL** extra após o último nome de arquivo. Esse formato permite que as caixas de diálogo no estilo Explorer retornem nomes de arquivo longos que incluem espaços. |
| Caixas de diálogo de estilo antigo      | As cadeias de caracteres de nome de arquivo e diretório são separadas por espaços. Para nomes de arquivo com espaços, a função usa nomes de arquivo curtos.                                                                                              |



 

Você pode usar a [**função FindFirstFile**](/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea) para converter entre nomes de arquivo longos e curtos.

Se você especificar **OFN \_ ALLOWMULTISELECT** e o usuário selecionar apenas um arquivo, a cadeia de caracteres **lpstrFile** não terá um separador entre o caminho e o nome do arquivo.

## <a name="filters"></a>Filtros

As informações contidas nesta seção aplicam-se às caixas de diálogo **abrir** e **salvar** no estilo do Explorer e estilo antigo.

Você pode fornecer filtros de nome de arquivo para ajudar o usuário a limitar os nomes de arquivo exibidos pela caixa de diálogo. Um filtro de nome de arquivo consiste em um par de cadeias de caracteres terminadas em nulo, uma descrição e um padrão, um concatenado ao outro. A caixa de diálogo exibe a descrição para permitir que o usuário escolha qual filtro usar; e ele usa o padrão para selecionar os arquivos a serem exibidos.

Para especificar os filtros, defina o membro **lpstrFilter** da estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) para apontar para um buffer que contém uma matriz de pares de cadeia de caracteres de filtro. A última cadeia de caracteres na matriz deve ser seguida por um caractere nulo extra.

Uma cadeia de caracteres de padrão pode ser uma combinação de caracteres de nome de arquivo válidos e o asterisco ( \* ). O asterisco é um caractere curinga que representa qualquer combinação de caracteres de nome de arquivo válidos. A caixa de diálogo exibe somente os arquivos que correspondem ao padrão. Para especificar vários padrões para a mesma descrição, você deve usar um ponto-e-vírgula (;) para separar os padrões. Observe que os caracteres de espaço na cadeia de caracteres de padrão podem produzir resultados inesperados.

O fragmento de código a seguir especifica dois filtros. O filtro com a descrição "Source" tem dois padrões. Se o usuário selecionar esse filtro, a caixa de diálogo exibirá somente os arquivos que têm o. C e. Extensões do CXX. Observe que, na linguagem de programação C, uma cadeia de caracteres entre aspas duplas é terminada em nulo.


```
OPENFILENAME ofn;       // common dialog box structure

ofn.lpstrFilter = "Source\0*.C;*.CXX\0All\0*.*\0"
ofn.nFilterIndex = 1;
```



O membro **nFilterIndex** da estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) especifica um índice que indica qual filtro a caixa de diálogo usa inicialmente. O primeiro filtro no buffer tem o índice 1, o segundo 2 e assim por diante. Se o usuário altera o filtro ao usar a caixa de diálogo, o **membro nFilterIndex** é definido como o índice do filtro selecionado no retorno.

Você pode criar um filtro personalizado definindo o membro **lpstrCustomFilter** como o endereço de um buffer que contém um único filtro e definindo o membro **nMaxCustFilter** para o tamanho do buffer, em caracteres ou bytes. A caixa de diálogo sempre coloca o filtro personalizado no início da lista de filtros e, no retorno, sempre atualiza a parte padrão do filtro com o padrão do filtro selecionado pelo usuário.

Para caixas de diálogo no estilo Explorer, a extensão padrão poderá ser alteração se o usuário selecionar um filtro diferente. Se o usuário selecionar um filtro cujo primeiro padrão é do formato \* .*xxx* (ou seja, a extensão não inclui um caractere curinga), a caixa de diálogo usa *xxx* como a extensão padrão. Isso ocorrerá somente se você tiver especificado uma extensão padrão no membro **lpstrDefExt** da [**estrutura OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) Por exemplo, se o usuário selecionar a "Origem \\ 0 \* . C; \* . Filtro CXX \\ 0", a extensão padrão muda para "C". No entanto, se você tiver definido o filtro como "Origem \\ 0 \* . C \* \\ 0", a extensão padrão não muda porque a extensão inclui um curinga.

A [**mensagem de \_ notificação CDN INCLUDEITEM**](cdn-includeitem.md) fornece outra maneira de filtrar os nomes que a caixa de diálogo exibe. Para usar essa mensagem, forneça um procedimento de gancho [**OFNHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) e especifique o sinalizador **OFN \_ ENABLEINCLUDENOTIFY** na estrutura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) ao criar a caixa de diálogo. Sempre que o usuário abre uma pasta, a caixa de diálogo envia uma **notificação CDN \_ INCLUDEITEM** para o procedimento de gancho para cada item na pasta recém-aberta. O valor de retorno do procedimento de gancho indica se a caixa de diálogo deve exibir o item na lista de itens da pasta.

## <a name="file-and-directory-validation"></a>Validação de arquivo e diretório

Exceto conforme observado, as informações nesta seção se aplicam às caixas de diálogo do estilo do Explorer e do estilo antigo **abrir** e **salvar como** .

A caixa de diálogo valida automaticamente os nomes de arquivo digitados pelo usuário para garantir que os nomes contenham apenas caracteres válidos. Para substituir a validação de caractere de nome de arquivo, defina o sinalizador **\_ novalidate OFN** .

Para forçar a caixa de diálogo a verificar se o usuário especificou o nome de um arquivo existente, defina o sinalizador **OFN \_ FILEMUSTEXIST** . Para forçar a verificação de que o caminho especificado existe, defina o sinalizador **OFN \_ PATHMUSTEXIST** . Se você definir o **sinalizador \_ CreatePrompt do OFN** , a caixa de diálogo solicitará ao usuário permissão para criar um arquivo inexistente. Se esse sinalizador for definido e o usuário optar por criar um novo arquivo, a caixa de diálogo será fechada e a função retornará o nome especificado. Caso contrário, a caixa de diálogo permanecerá aberta.

Ao usar a caixa de diálogo **salvar como** , você pode direcionar a caixa de diálogo para solicitar ao usuário permissão para substituir um arquivo existente, definindo o sinalizador **OFN \_ OVERWRITEPROMPT** .

Por padrão, a caixa de diálogo cria um arquivo de teste de comprimento zero para determinar se um novo arquivo pode ser criado no diretório selecionado. Para evitar a criação desse arquivo de teste, defina o sinalizador **OFN \_ NOTESTFILECREATE** .

Se você habilitar um procedimento de gancho, a caixa de diálogo notificará seu procedimento de gancho quando ocorrer uma violação de compartilhamento de rede para o nome de arquivo especificado pelo usuário. Se você definir o sinalizador **OFN \_ Explorer** , a caixa de diálogo enviará a mensagem [**\_ SHAREVIOLATION da CDN**](cdn-shareviolation.md) para o procedimento de gancho. Se você não definir o **OFN \_ Explorer**, a caixa de diálogo enviará a mensagem registrada [**SHAREVISTRING**](sharevistring.md) para o procedimento de gancho. Para impedir que a caixa de diálogo envie notificações para compartilhamento de violações, defina o sinalizador **OFN \_ SHAREAWARE** .

Se o usuário marcar a caixa de seleção somente leitura, a caixa de diálogo definirá o sinalizador **OFN \_ ReadOnly** no retorno. Para ocultar a **caixa de seleção Abrir como Somente** Leitura, de definido o sinalizador **OFN \_ HIDEREADONLY.** Para impedir que a caixa de diálogo retorne nomes de arquivos existentes que têm o atributo somente leitura, de definir o sinalizador **OFN \_ NOREADONLYRETURN.**

Para impedir que a caixa de diálogo desreferencie arquivos de link, defina o **valor OFN \_ NODEREFERENCELINKS.** Nesse caso, a caixa de diálogo retorna o nome do arquivo de link em vez do nome do arquivo referenciado pelo arquivo de link.

## <a name="open-and-save-as-dialog-box-customization"></a>Personalização da caixa de diálogo Abrir e Salvar como

Você pode personalizar uma **caixa de** diálogo Abrir ou Salvar **como** fornecendo um procedimento de gancho, um modelo personalizado ou ambos. No entanto, as versões de estilo explorer e de estilo antigo das caixas de diálogo diferem no uso de modelos personalizados e procedimentos de gancho.

Para obter informações sobre como personalizar uma caixa de diálogo no estilo Explorer, consulte Procedimentos de gancho no estilo [Explorer,](#explorer-style-hook-procedures)Modelos [Personalizados](#explorer-style-custom-templates)no Estilo Explorer e Identificadores de Controle de Estilo [Explorer](#explorer-style-control-identifiers). Para obter informações sobre como personalizar uma caixa de diálogo de estilo antigo, consulte [Personalização Old-Style caixas de diálogo](#customizing-old-style-dialog-boxes).

A tabela a seguir resume as diferenças entre os dois estilos.



| Personalização                  | Description                                                                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Procedimento de gancho no estilo explorer  | O procedimento de gancho recebe mensagens de notificação enviadas da caixa de diálogo comum e mensagens para quaisquer controles adicionais que você definiu especificando um modelo de caixa de diálogo filho. O procedimento de gancho não recebe mensagens para os controles padrão da caixa de diálogo padrão. |
| Modelo personalizado no estilo explorer | O sistema usa o modelo personalizado para criar uma caixa de diálogo filho. O modelo pode definir controles adicionais e pode especificar o local do cluster de controles padrão. O modelo personalizado não substitui o modelo padrão.                                          |
| Procedimento de gancho de estilo antigo       | O procedimento de gancho recebe todas as mensagens enviadas para a caixa de diálogo, incluindo mensagens para os controles padrão e todos os controles personalizados. O procedimento de gancho também recebe mensagens registradas enviadas da caixa de diálogo comum.                                                         |
| Modelo personalizado de estilo antigo      | O modelo personalizado substitui o modelo padrão. Crie o modelo personalizado modificando o modelo padrão especificado no arquivo FileOpen. Dlg.                                                                                                                                  |



 

O título padrão para as caixas de diálogo estilo do Explorer e estilo antigo é "**abrir**" ou "**salvar como**". Para alterar o título, especifique o novo título no membro **lpstrTitle** da estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .

O hive do registro do **\_ \_ usuário do HKEY Current** do usuário pode conter valores que personalizam o conteúdo das caixas de diálogo **abrir** e **salvar como** do Gerenciador de navegador. Essas entradas de registro afetam apenas as caixas de diálogo exibidas para o usuário associado ao hive do registro.

Para ocultar os recursos das caixas de diálogo **abrir** e **salvar como** do estilo do Explorer, um administrador pode definir os valores na tabela a seguir nesta subchave:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Comdlg32
```



| Nome do valor       | Valor | Significado                                  |
|------------------|-------|------------------------------------------|
| **NoPlacesBar**  | 1     | Oculta a barra de locais.                    |
| **NoFileMRU**    | 1     | Oculta a lista de MRU (usada mais recentemente). |
| **NoBackButton** | 1     | Oculta o botão **voltar** .               |



 

O conteúdo da barra de **locais** é determinado pelo conteúdo da seguinte subchave:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Comdlg32
                     Placesbar
```

No momento, só pode haver cinco entradas sob essa chave, e o índice de valor/nome é baseado em zero. Os nomes das entradas devem ser Place0, Place1, Place2, Place3 e Place4. Os valores das entradas podem ser valores **reg \_ DWORD**, **reg \_ sz** ou **reg \_ expande \_ sz** que identificam os locais a serem incluídos na barra de locais.



| Tipo de valor                         | Significado                                                                                                   |
|------------------------------------|-----------------------------------------------------------------------------------------------------------|
| **REG \_ DWORD**                     | Um valor de CSIDl que identifica uma pasta. Para ver uma lista de valores CSIDL, confira [**Valores CSIDL**](../shell/csidl.md). |
| **REG \_ SZ** ou **REG \_ EXPAND \_ SZ** | Uma cadeia de caracteres terminada em nulo que especifica um caminho válido.                                                     |



 

## <a name="explorer-style-hook-procedures"></a>Explorer-Style de gancho

Você pode personalizar uma caixa de diálogo **Abrir** ou Salvar **como** no estilo Explorer fornecendo um procedimento de gancho, um modelo personalizado ou ambos. Se você fornecer um procedimento de gancho para uma caixa de diálogo no estilo Explorer, o sistema criará uma caixa de diálogo que é um filho da caixa de diálogo padrão. O procedimento de gancho atua como o procedimento de diálogo para a caixa de diálogo filho. Essa caixa de diálogo filho é baseada no modelo personalizado ou em um modelo padrão, se nenhum for fornecido. Para obter mais informações, consulte [Modelos personalizados no estilo explorer.](#explorer-style-custom-templates)

Para habilitar um procedimento  de gancho para uma caixa de diálogo Abrir ou Salvar **como** no estilo Explorer, use a estrutura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) ao criar a caixa de diálogo. De definir os sinalizadores **OFN \_ ENABLEHOOK** e **OFN \_ EXPLORER** no membro **Flags** e especifique o endereço de um procedimento de gancho [**OFNHookProc**](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) no membro **lpfnHook.** Se você fornecer um procedimento de gancho e omitir o sinalizador **OFN \_ EXPLORER,** deverá usar um procedimento de gancho [**OFNHookProcOldStyle**](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) e obter a interface do usuário de estilo antigo. Para obter mais informações, consulte [Personalização Old-Style caixas de diálogo](#customizing-old-style-dialog-boxes).

Um procedimento de gancho no estilo Explorer recebe uma variedade de mensagens enquanto a caixa de diálogo está aberta. Entre elas estão as seguintes:

-   A [**mensagem WM \_ INITDIALOG**](wm-initdialog.md) e outras mensagens da caixa de diálogo padrão, como a mensagem de cor do controle [**WM \_ CTLCOLORDLG.**](wm-ctlcolordlg.md)
-   Um conjunto de [**mensagens de \_ notificação WM NOTIFY**](../controls/wm-notify.md) indicando ações realizadas pelo usuário ou outros eventos de caixa de diálogo.
-   Mensagens para quaisquer controles adicionais que você definiu especificando um modelo de caixa de diálogo filho.

Além disso, há um conjunto de mensagens que você pode enviar para uma caixa de diálogo no estilo Explorer para obter informações ou para controlar o comportamento e a aparência da caixa de diálogo.

Se você fornecer um procedimento de gancho para uma caixa de diálogo estilo de Gerenciador, o procedimento de caixa de diálogo padrão criará uma caixa de diálogo filho quando o procedimento de diálogo padrão estiver processando sua mensagem [**\_ INITDIALOG do WM**](wm-initdialog.md) . O procedimento de gancho atua como o procedimento de diálogo para a caixa de diálogo filho. Neste momento, o procedimento de gancho recebe sua própria **mensagem \_ INITDIALOG do WM** com o parâmetro *lParam* definido como o endereço da estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) usada para inicializar a caixa de diálogo. Depois que a caixa de diálogo filho terminar de processar sua própria mensagem do **WM \_ INITDIALOG** , o procedimento de diálogo padrão moverá os controles padrão, se necessário, para liberar espaço para qualquer controle adicional da caixa de diálogo filho. Em seguida, o procedimento de caixa de diálogo padrão envia a mensagem de notificação [**\_ INITDONE da CDN**](cdn-initdone.md) para o procedimento de gancho.

O procedimento de gancho recebe mensagens de notificação do [**WM \_ notificar**](../controls/wm-notify.md) que indicam ações executadas pelo usuário na caixa de diálogo. Você pode usar algumas dessas mensagens para controlar o comportamento da caixa de diálogo. Por exemplo, o procedimento de gancho recebe a mensagem [**\_ FILEOK da CDN**](cdn-fileok.md) quando o usuário escolhe um nome de arquivo e clica no botão **OK** . Em resposta a essa mensagem, o procedimento de gancho pode usar a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para rejeitar o nome selecionado e forçar a caixa de diálogo a permanecer aberta.

O parâmetro *lParam* para cada mensagem de [**\_ notificação do WM**](../controls/wm-notify.md) é um ponteiro para uma estrutura [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) ou [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) que define a ação. O membro do **código** no cabeçalho dessa estrutura contém uma das seguintes mensagens de notificação.



| Mensagem                                           | Significado                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_FILEOK CDN**](cdn-fileok.md)                 | O usuário clicou no botão **OK** ; a caixa de diálogo está prestes a fechar.                                                                                                                                                                                                                          |
| [**\_FOLDERCHANGE CDN**](cdn-folderchange.md)     | O usuário abriu uma nova pasta ou diretório.                                                                                                                                                                                                                                                     |
| [**ajuda da CDN \_**](cdn-help.md)                     | O usuário clicou no botão **ajuda** .                                                                                                                                                                                                                                                          |
| [**CDN \_ INCLUDEITEM**](cdn-includeitem.md)       | Determina se um item deve ser exibido. Quando o usuário abre uma nova pasta ou diretório, o sistema envia essa notificação para cada item na pasta ou diretório. O sistema enviará essa notificação somente se **o sinalizador OFN \_ ENABLEINCLUDENOTIFY** tiver sido definido.                          |
| [**CDN \_ INITDONE**](cdn-initdone.md)             | O sistema concluiu a inicialização da caixa de diálogo e a caixa de diálogo concluiu o processamento da mensagem [**WM \_ INITDIALOG.**](wm-initdialog.md) Além disso, o sistema concluiu a organização de controles na caixa de diálogo comum para dar espaço aos controles da caixa de diálogo filho (se algum). |
| [**CDN \_ SELCHANGE**](cdn-selchange.md)           | O usuário selecionou um novo arquivo ou pasta na lista de arquivos.                                                                                                                                                                                                                                     |
| [**COMPARTILHAMENTO \_ DE CDNVIOLATION**](cdn-shareviolation.md) | A caixa de diálogo comum encontrou uma violação de compartilhamento no arquivo prestes a ser retornado.                                                                                                                                                                                                        |
| [**TYPECHANGE DA CDN \_**](cdn-typechange.md)         | O usuário selecionou um novo tipo de arquivo na lista de tipos de arquivo.                                                                                                                                                                                                                                 |



 

Essas [**mensagens WM \_ NOTIFY**](../controls/wm-notify.md) superam as mensagens registradas [**FILEOKSTRING**](fileokstring.md), [**LBSELCHSTRING,**](lbselchstring.md) [**SHAREVISTRING**](sharevistring.md)e [**HELPMSGSTRING**](helpmsgstring.md) usadas por versões anteriores das caixas de diálogo Abrir e Salvar **como.**  No entanto, o procedimento de gancho também receberá a mensagem sobressalo após a mensagem **WM \_ NOTIFY** se o processamento **WM \_ NOTIFY** não usar [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) para definir um valor **\_ MSGRESULT** de DWL não zero.

Para recuperar informações sobre o status da caixa de diálogo ou para controlar o comportamento e a aparência da caixa de diálogo, o procedimento de gancho pode enviar as mensagens a seguir para a caixa de diálogo.



| Mensagem                                             | Significado                                                                                                                                                                                                                  |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CDM \_ GETFILEPATH**](cdm-getfilepath.md)         | Recupera o caminho e o nome do arquivo selecionado.                                                                                                                                                                   |
| [**CDM \_ GETFOLDERIDLIST**](cdm-getfolderidlist.md) | Recupera a lista de identificadores de item correspondente à pasta atual que a caixa de diálogo tem aberta. Para obter mais informações sobre listas de identificadores de itens, consulte [Introduction to the Shell namespace](/windows/desktop/shell/namespace-intro). |
| [**CDM \_ GETfolderpath**](cdm-getfolderpath.md)     | Recupera o caminho da pasta ou diretório atual para a caixa de diálogo.                                                                                                                                                |
| [**CDM \_ GETspec**](cdm-getspec.md)                 | Recupera o nome do arquivo (não incluindo o caminho) do arquivo selecionado no momento na caixa de diálogo.                                                                                                                       |
| [**CDM \_ HIDECONTROL**](cdm-hidecontrol.md)         | Oculta o controle especificado.                                                                                                                                                                                             |
| [**CDM \_ SETCONTROLTEXT**](cdm-setcontroltext.md)   | Define o texto no controle especificado.                                                                                                                                                                                  |
| [**CDM \_ SETDEFEXT**](cdm-setdefext.md)             | Define a extensão de nome de arquivo padrão para a caixa de diálogo.                                                                                                                                                                 |



 

## <a name="explorer-style-custom-templates"></a>Explorer-Style modelos personalizados

Para definir controles adicionais para uma caixa de diálogo **abrir** ou **salvar como** do estilo do Explorer, use a estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) para especificar um modelo para uma caixa de diálogo filho que contenha os controles adicionais. Se o seu modelo de caixa de diálogo filho for um recurso em um aplicativo ou em uma biblioteca de vínculo dinâmico, defina o sinalizador **OFN \_ ENABLETEMPLATE** no membro **flags** e use os membros **HINSTANCE** e **lpTemplateName** da estrutura para identificar o módulo e o nome do recurso. Se o modelo já estiver na memória, defina o sinalizador **OFN \_ ENABLETEMPLATEHANDLE** e use o membro **HINSTANCE** para identificar o objeto de memória que contém o modelo. Ao fornecer um modelo de diálogo filho para uma caixa de diálogo estilo de Gerenciador, você também deve definir o sinalizador **OFN \_ Explorer** ; caso contrário, o sistema pressupõe que você está fornecendo um modelo de substituição para uma caixa de diálogo estilo antigo. Normalmente, se você fornecer controles adicionais, também deverá fornecer um [procedimento de gancho de estilo de Explorer](#explorer-style-hook-procedures) para processar mensagens para os novos controles.

Você pode criar seu modelo de caixa de diálogo filho como qualquer outro modelo, exceto que você deve especificar os **estilos \_ WS Child** e **WS \_ CLIPSIBLINGS** e deve especificar os estilos de **\_ controle** **DS \_ 3DLOOK** e DS. O sistema requer o **estilo FILHO \_ do WS** porque seu modelo define uma caixa de diálogo filho da caixa de diálogo Padrão **Abrir** ou Salvar **como.** O **estilo WS \_ CLIPSIBLINGS** garante que a caixa de diálogo filho não pinta em nenhum dos controles na caixa de diálogo padrão. O **estilo DS \_ 3DLOOK** garante que a aparência dos controles na caixa de diálogo filho seja consistente com os controles na caixa de diálogo padrão. O **estilo DS \_ CONTROL** garante que o usuário possa usar a TAB e outras chaves de navegação para se mover entre todos os controles, padrão ou personalizado, na caixa de diálogo personalizada.

Para dar espaço aos novos controles, o sistema expande a caixa de diálogo padrão pela largura e altura da caixa de diálogo personalizada. Por padrão, todos os controles da caixa de diálogo personalizada são posicionados abaixo dos controles na caixa de diálogo padrão. No entanto, você pode substituir esse posicionamento padrão incluindo um controle de texto estático em seu modelo de caixa de diálogo personalizado e atribuindo a ele o valor do identificador de controle **stc32**. (Esse valor é definido no arquivo de header Dlgs.h.) Nesse caso, o sistema usa o controle como ponto de referência para determinar onde posicionar os novos controles. Todos os novos controles acima e à esquerda do controle **stc32** são posicionados na mesma quantidade acima e à esquerda dos controles na caixa de diálogo padrão. Novos controles abaixo e à direita do **controle stc32** são posicionados abaixo e à direita dos controles padrão. Em geral, cada novo controle é posicionado para que ele tenha a mesma posição em relação aos controles padrão que tinha com o **controle stc32.** Para dar espaço a esses novos controles, o sistema adiciona espaço à esquerda, à direita, à parte inferior e à parte superior da caixa de diálogo padrão, conforme necessário.

O sistema requer o procedimento de gancho para processar todas as mensagens destinadas à caixa de diálogo personalizada e, portanto, envia as mesmas mensagens de janela para o procedimento de gancho como qualquer outro procedimento de caixa de diálogo. Por exemplo, o procedimento de gancho recebe mensagens de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) quando o usuário clica nos controles de botão na caixa de diálogo personalizada. O procedimento de gancho é responsável por inicializar esses controles e recuperar valores dos controles quando a caixa de diálogo é fechada. Observe que quando o procedimento de gancho recebe a mensagem [**\_ INITDIALOG do WM**](wm-initdialog.md) , o sistema ainda não moveu os controles para suas posições finais.

O procedimento de caixa de diálogo padrão manipula mensagens para todos os controles na caixa de diálogo padrão, mas o procedimento de gancho recebe as mensagens de notificação para ações do usuário nesses controles, conforme descrito em [procedimentos de gancho no estilo do Explorer](#explorer-style-hook-procedures).

## <a name="explorer-style-control-identifiers"></a>Identificadores de controle de Explorer-Style

O SDK (Software Development Kit) do Windows fornece o modelo de caixa de diálogo padrão para as caixas de diálogo de estilo antigo, mas não inclui o modelo padrão para as caixas de diálogo de estilo de navegador. Isso ocorre porque as caixas de diálogo do estilo Explorer permitem que você adicione seus próprios controles, mas não oferece suporte à modificação do modelo para os controles padrão. No entanto, em alguns casos, talvez seja necessário saber os identificadores de controle usados nos modelos padrão. Por exemplo, as mensagens [**CDM \_ HIDECONTROL**](cdm-hidecontrol.md) e [**CDM \_ SETCONTROLTEXT**](cdm-setcontroltext.md) exigem um identificador de controle.

A tabela a seguir mostra os identificadores dos controles padrão nas caixas de diálogo **abrir** no estilo do Gerenciador e **salvar como** . Os identificadores são constantes definidas em Dlgs. h e WinUser. h.



| Identificador de controle | Descrição do controle                                                                                                                                                                                                                                                                        |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **chx1**           | A caixa de seleção somente leitura                                                                                                                                                                                                                                                                    |
| **cmb1**           | Caixa de combinação suspensa que exibe a lista de filtros de tipo de arquivo                                                                                                                                                                                                                            |
| **stc2**           | Rótulo da caixa de combinação **cmb1**                                                                                                                                                                                                                                                           |
| **cmb2**           | Caixa de combinação listada que exibe a unidade ou pasta atual e que permite que o usuário selecione uma unidade ou pasta para abrir                                                                                                                                                                |
| **stc4**           | Rótulo para a **caixa de combinação cmb2**                                                                                                                                                                                                                                                           |
| **cmb13**          | Caixa de combinação listada que exibe o nome do arquivo atual, permite que o usuário digite o nome de um arquivo a ser aberto e selecione um arquivo que foi aberto ou salvo recentemente. Isso é para aplicativos anteriores compatíveis com o Explorer sem gancho ou modelo de caixa de diálogo. Compare com **edt1.** |
| **edt1**           | Controle de edição que exibe o nome do arquivo atual ou permite que o usuário digite o nome do arquivo a ser aberto. Compare com **cmb13**.                                                                                                                                                  |
| **stc3**           | Rótulo para a **caixa de combinação cmb13** e o controle de edição edt1                                                                                                                                                                                                                                |
| **lst1**           | Caixa de listagem que exibe o conteúdo da unidade ou pasta atual                                                                                                                                                                                                                         |
| **stc1**           | Rótulo da caixa **de listagem lst1**                                                                                                                                                                                                                                                            |
| **Idok**           | O **botão de** comando OK (botão de push)                                                                                                                                                                                                                                                    |
| **Idcancel**       | O botão de comando **Cancelar** (botão de ação)                                                                                                                                                                                                                                                |
| **pshHelp**        | O botão de comando **ajuda** (botão de ação)                                                                                                                                                                                                                                                  |



 

## <a name="customizing-old-style-dialog-boxes"></a>Personalizando caixas de diálogo de Old-Style

Você pode personalizar uma caixa de diálogo **abrir** ou **salvar como** de estilo antigo, fornecendo um procedimento de gancho [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) que recebe mensagens ou notificações destinadas ao procedimento de caixa de diálogo padrão. Você também pode fornecer um modelo personalizado para usar no lugar do modelo padrão. Os procedimentos de gancho e os modelos usados com as caixas de diálogo de estilo antigo são semelhantes aos usados com as outras caixas de diálogo comuns. Para obter mais informações, consulte [procedimentos de conexão para caixas de diálogo comuns](customizing-common-dialog-boxes.md) e [modelos personalizados](customizing-common-dialog-boxes.md).

Para habilitar um procedimento de gancho para uma caixa de diálogo **abrir** ou **salvar como** de estilo antigo, use a estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) ao criar a caixa de diálogo. Defina o **sinalizador OFN \_ ENABLEHOOK** no membro **flags** e especifique o endereço de um procedimento de gancho [*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) no membro **lpfnHook** . O procedimento da caixa de diálogo envia uma mensagem do [**WM \_ INITDIALOG**](wm-initdialog.md) para o procedimento de gancho com o parâmetro *param* definido como o endereço da estrutura **da OPENFILENAME** usada para inicializar a caixa de diálogo.

Você pode usar a estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) para especificar um modelo personalizado para a caixa de diálogo **abrir** ou **salvar como** a ser usada no lugar do modelo padrão. Se seu modelo personalizado for um recurso em um aplicativo ou em uma biblioteca de vínculo dinâmico, defina o sinalizador **OFN \_ ENABLETEMPLATE** no membro **flags** e use os membros **HINSTANCE** e **lpTemplateName** da estrutura para identificar o módulo e o nome do recurso. Se o modelo personalizado já estiver na memória, defina o sinalizador **OFN \_ ENABLETEMPLATEHANDLE** e use o membro **HINSTANCE** para identificar o objeto de memória que contém o modelo. Crie o modelo personalizado modificando o modelo padrão especificado no arquivo Fileopen.dlg. Os identificadores de controle usados nos modelos de caixa de diálogo Padrão De encontrar e substituir são definidos no arquivo Dlgs.h.

Por padrão, as [**funções GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) e [**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea) exibem as caixas de diálogo no estilo Explorer. Se você quiser exibir uma caixa de diálogo de estilo antigo, deverá fornecer um procedimento de gancho [**OFNHookProcOldStyle**](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85)) e garantir que o sinalizador **OFN \_ EXPLORER** não está definido no membro **Flags** da estrutura [**OPENFILENAME.**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)

Se você definir o **sinalizador OFN \_ EXPLORER,** o sistema tratará um procedimento de gancho ou um modelo personalizado como uma personalização no estilo Explorer. Para obter informações sobre como personalizar uma caixa de diálogo no estilo Explorer, consulte [Modelos personalizados no estilo explorer.](#explorer-style-custom-templates)

## <a name="see-also"></a>Confira também

* [O arquivo está em uso de exemplo](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/fileisinuse)