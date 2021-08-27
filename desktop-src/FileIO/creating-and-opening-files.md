---
description: Considerações para criar ou abrir um arquivo usando a função CreateFile.
ms.assetid: 094cac29-c66d-409e-8928-878dc693d393
title: Criando e abrindo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e80449942fbceb39c37604bf6d8b5410d171d195
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469923"
---
# <a name="creating-and-opening-files"></a>Criando e abrindo arquivos

A [**função CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) pode criar um novo arquivo ou abrir um arquivo existente. Você deve especificar o nome do arquivo, as instruções de criação e outros atributos. Quando um aplicativo cria um novo arquivo, o sistema operacional o adiciona ao diretório especificado.

O sistema operacional atribui um identificador exclusivo, chamado de identificador *,* a cada arquivo que é aberto ou criado usando [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). Um aplicativo pode usar esse handle com funções que leem, escrevem e descrevem o arquivo. Ela é válida até que todas as referências a esse alça sejam fechadas. Quando um aplicativo é iniciado, ele herda todos os alças abertas do processo que o iniciou se os alças foram criados como herdáveis.

Um aplicativo deve verificar o valor do alça retornado por [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) antes de tentar usar o alça para acessar o arquivo. Se ocorrer um erro, o valor do handle será **INVALID \_ HANDLE \_ VALUE** e o aplicativo poderá usar a [**função GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter informações de erro estendidas.

Quando um aplicativo usa [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), ele deve usar o parâmetro *dwDesiredAccess* para especificar se ele pretende ler do arquivo, gravar no arquivo, ler e gravar ou não. Isso é conhecido como solicitar um *modo de acesso*. O aplicativo também deve usar o parâmetro *dwCreationDisposition* para especificar qual ação deve ser tomada se o arquivo já existir, conhecido como a disposição *de criação*. Por exemplo, um aplicativo pode chamar **CreateFile** com *dwCreationDisposition* definido como **CREATE \_ ALWAYS** para sempre criar um novo arquivo, mesmo se já existir um arquivo com o mesmo nome (assim, sobrescrever o arquivo existente). Se isso for bem-sucedido ou não dependerá de fatores como atributos e configurações de segurança do arquivo anterior (consulte as seções a seguir para obter mais informações).

Um aplicativo também usa [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para especificar se deseja compartilhar o arquivo para leitura, escrita, ambos ou nenhum deles. Isso é conhecido como o modo *de compartilhamento*. Um arquivo aberto que não é compartilhado (*dwShareMode* definido como zero) não pode ser aberto novamente, seja pelo aplicativo que o abriu ou por outro aplicativo, até que seu handle tenha sido fechado. Isso também é conhecido como acesso exclusivo.

Quando um processo usa [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para tentar abrir um arquivo que já foi aberto em um modo de compartilhamento (*dwShareMode* definido como um valor não zero válido), o sistema compara os modos de acesso e compartilhamento solicitados com aqueles especificados quando o arquivo foi aberto. Se você especificar um modo de acesso ou compartilhamento que entre em conflito com os modos especificados na chamada anterior, **CreateFile** falhará.

A tabela a seguir ilustra as combinações válidas de duas chamadas para [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) usando vários modos de acesso e modos de compartilhamento (*dwDesiredAccess*, *dwShareMode,* respectivamente). Não importa em qual ordem as **chamadas CreateFile** são feitas. No entanto, quaisquer operações de E/S de arquivo subsequentes em cada alça de arquivo ainda serão restritas pelos modos atuais de acesso e compartilhamento associados a esse determinado alça de arquivo.




| Primeira chamada para <a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong>CreateFile</strong></a> | Segunda chamada válida para <a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong>CreateFile</strong></a> | 
|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 
| <strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong><br /> | <ul><li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li><li><strong>GENERIC_READ</strong> | <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong> | <strong>FILE_SHARE_WRITE</strong></li></ul> | 




 

Além dos atributos de arquivo padrão, você também pode especificar atributos de segurança incluindo um ponteiro para uma estrutura [**SECURITY \_ ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) como o quarto parâmetro [**de CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). No entanto, o sistema de arquivos subjacente deve dar suporte à segurança para que isso tenha algum efeito (por exemplo, o sistema de arquivos NTFS dá suporte a ele, mas os vários sistemas de arquivos FAT não têm). Para obter mais informações sobre atributos de segurança, consulte [Controle de acesso](/windows/desktop/SecAuthZ/access-control).

Um aplicativo que cria um novo arquivo pode fornecer um handle opcional para um arquivo de modelo, do qual [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) recebe atributos de arquivo e atributos estendidos para a criação do novo arquivo.

## <a name="createfile-scenarios"></a>Cenários de CreateFile

Há vários cenários fundamentais para iniciar o acesso a um arquivo usando a [**função CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Eles são resumidos como:

-   Criar um novo arquivo quando um arquivo com esse nome ainda não existir.
-   Criar um novo arquivo mesmo que já exista um arquivo com o mesmo nome, limpando seus dados e iniciando vazio.
-   Abrir um arquivo existente somente se ele existir e apenas intacto.
-   Abrir um arquivo existente somente se ele existir, truncando-o para que ele seja vazio.
-   Abrir um arquivo sempre: como está se ele existir, criando um novo se ele não existir.

Esses cenários são controlados pelo uso adequado do parâmetro *dwCreationDisposition* . Abaixo está uma análise de como esses cenários são mapeados para valores para esse parâmetro e o que acontece quando eles são usados.

Ao criar ou abrir um novo arquivo quando um arquivo com esse nome ainda não existir (*dwCreationDisposition* definido como **criar \_ novo**, **criar \_ sempre** ou **abrir \_ sempre**), a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) executará as seguintes ações:

-   Combina os atributos de arquivo e os sinalizadores especificados por *dwFlagsAndAttributes* com o arquivo de **\_ atributo \_ File**.
-   Define o comprimento do arquivo como zero.
-   Copia os atributos estendidos fornecidos pelo arquivo de modelo para o novo arquivo se o parâmetro *hTemplateFile* for especificado (isso substitui todos os sinalizadores de **\_ atributo \_ \* de arquivo** especificados anteriormente).
-   Define o sinalizador de herança especificado pelo membro **bInheritHandle** e o descritor de segurança especificado pelo membro **LpSecurityDescriptor** do parâmetro *lpSecurityAttributes* (estrutura de [**\_ atributos de segurança**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) ), se fornecido.

Ao criar um novo arquivo, mesmo que já exista um arquivo com o mesmo nome (*dwCreationDisposition* definido como **Create \_ Always**), a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) executará as seguintes ações:

-   Verifica os atributos de arquivo atuais e as configurações de segurança para acesso de gravação, falhando se negado.
-   Combina os atributos de arquivo e os sinalizadores especificados por *dwFlagsAndAttributes* com o arquivo de **\_ atributo File \_** e os atributos de arquivo existentes.
-   Define o comprimento do arquivo como zero (ou seja, quaisquer dados que estavam no arquivo não estão mais disponíveis e o arquivo está vazio).
-   Copia os atributos estendidos fornecidos pelo arquivo de modelo para o novo arquivo se o parâmetro *hTemplateFile* for especificado (isso substitui todos os sinalizadores de **\_ atributo \_ \* de arquivo** especificados anteriormente).
-   Define o sinalizador Inherit especificado pelo membro **bInheritHandle** do parâmetro *lpSecurityAttributes* (estrutura de [**\_ atributos de segurança**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) ), se fornecido, mas ignora o membro **lpSecurityDescriptor** da estrutura **de \_ atributos de segurança** .
-   Se for bem-sucedida (ou seja, [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) retornar um identificador válido), chamar [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) produzirá o erro de código **\_ já \_ existe**, mesmo que para esse caso de uso específico, na verdade, ele não é um erro como tal (se você pretende criar um arquivo "novo" (vazio) no lugar do existente).

Ao abrir um arquivo existente (*dwCreationDisposition* definido como **abrir \_ existente**, **abrir \_ sempre** ou **truncar o \_ existente**), a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) executa as seguintes ações:

-   Verifica os atributos de arquivo atuais e as configurações de segurança para acesso solicitado, falhando se negado.
-   Combina os sinalizadores de arquivo (**\_ sinalizador \_ \* de arquivo* _) especificados por _dwFlagsAndAttributes * com os atributos de arquivo existentes e ignora os atributos de arquivo (* * \_ atributo \_ \* de arquivo* _) especificado por _dwFlagsAndAttributes *.
-   Define o comprimento do arquivo como zero somente se *dwCreationDisposition* estiver definido como **truncar \_ existente**, caso contrário, o tamanho do arquivo atual será mantido e o arquivo será aberto no estado em que se encontra.
-   Ignora o parâmetro *hTemplateFile* .
-   Define o sinalizador Inherit especificado pelo membro **bInheritHandle** do parâmetro *lpSecurityAttributes* (estrutura de [**\_ atributos de segurança**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) ), se fornecido, mas ignora o membro **lpSecurityDescriptor** da estrutura **de \_ atributos de segurança** .

## <a name="file-attributes-and-directories"></a>Atributos e diretórios de arquivo

Os atributos de arquivo fazem parte dos metadados associados a um arquivo ou diretório, cada um com sua própria finalidade e regras sobre como ele pode ser definido e alterado. Alguns desses atributos se aplicam somente a arquivos e alguns apenas aos diretórios. Por exemplo, o atributo de **\_ \_ diretório de atributo File** aplica-se somente a diretórios: ele é usado pelo sistema de arquivos para determinar se um objeto no disco é um diretório, mas não pode ser alterado para um objeto do sistema de arquivos existente.

Alguns atributos de arquivo podem ser definidos para um diretório, mas têm significado apenas para arquivos criados nesse diretório, agindo como atributos padrão. Por exemplo, **o \_ atributo de arquivo \_ compactado** pode ser definido em um objeto de diretório, mas como o próprio objeto de diretório não contém dados reais, ele não é realmente compactado; no entanto, os diretórios marcados com esse atributo dizem ao sistema de arquivos para compactar todos os novos arquivos adicionados a esse diretório. Qualquer atributo de arquivo que possa ser definido em um diretório e também será definido para novos arquivos adicionados a esse diretório é conhecido como um *atributo herdado*.

A função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) fornece um parâmetro para definir determinados atributos de arquivo quando um arquivo é criado. Em geral, esses atributos são os mais comuns para um aplicativo usar no momento da criação do arquivo, mas nem todos os atributos de arquivo possíveis estão disponíveis para **CreateFile**. Alguns atributos de arquivo exigem o uso de outras funções, como [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa), [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)ou [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) depois que o arquivo já existe. No caso do **diretório de \_ atributos \_ de arquivo**, a função [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) é necessária no momento da criação porque **CreateFile** não pode criar diretórios. Os outros atributos de arquivo que exigem tratamento especial são o **\_ \_ \_ ponto de nova análise de atributo de arquivo** e o **\_ \_ \_ arquivo esparso de atributo de arquivo**, que exigem **DeviceIoControl**. Para obter mais informações, consulte [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa).

Como mencionado anteriormente, a herança de atributo de arquivo ocorre quando um arquivo é criado com atributos de arquivo lidos dos atributos de diretório em que o arquivo será localizado. A tabela a seguir resume esses atributos herdados e como eles se relacionam com os recursos de [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .



| Estado do atributo de diretório                                      | Funcionalidade de substituição de herança [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para novos arquivos      |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| Do **arquivo \_ ATRIBUTO \_ compactado** definido.<br/>                | Sem controle. Use [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) para limpar.<br/>    |
| Do **arquivo \_ ATRIBUTO \_ compactado** não definido.<br/>            | Sem controle. Use [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) para definir.<br/>      |
| Do **arquivo \_ ATRIBUTO \_ criptografado** conjunto.<br/>                 | Sem controle. Use [**DecryptFile**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea).<br/>                      |
| Do **arquivo \_ ATRIBUTO \_ criptografado** não definido.<br/>             | Pode ser definido usando [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).<br/>                       |
| Do **arquivo \_ ATRIBUTO \_ sem \_ conteúdo \_ indexado** definido.<br/>     | Sem controle. Use [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) para limpar.<br/> |
| Do **arquivo \_ ATRIBUTO \_ sem \_ conteúdo \_ indexado** não definido.<br/> | Sem controle. Use [**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) para definir.<br/>   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controle de acesso](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**Constantes de atributo de arquivo**](file-attribute-constants.md)
</dt> <dt>

[Compactação e descompactação de arquivos](file-compression-and-decompression.md)
</dt> <dt>

[Criptografia de Arquivo](file-encryption.md)
</dt> <dt>

[Funções de gerenciamento de arquivos](file-management-functions.md)
</dt> <dt>

[Identificadores e objetos](/windows/desktop/SysInfo/handles-and-objects)
</dt> <dt>

[Manipular herança](/windows/desktop/SysInfo/handle-inheritance)
</dt> <dt>

[Abrir um arquivo para leitura ou gravação](opening-a-file-for-reading-or-writing.md)
</dt> <dt>

[**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> </dl>

 

