---
Description: Os atributos de arquivo são valores de metadados armazenados pelo sistema de arquivos no disco e são usados pelo sistema e estão disponíveis para desenvolvedores por meio de várias APIs de e/s de arquivo.
ms.assetid: ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156
title: Constantes de atributo de arquivo (WinNT. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
ms.openlocfilehash: eae376462ae6c633be96e4434fbb782fa41c802f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756941"
---
# <a name="file-attribute-constants"></a>Constantes de atributo do arquivo

Os atributos de arquivo são valores de metadados armazenados pelo sistema de arquivos no disco e são usados pelo sistema e estão disponíveis para desenvolvedores por meio de várias APIs de e/s de arquivo. Para obter uma lista de APIs e tópicos relacionados, consulte a seção Consulte também.

## <a name="example"></a>Exemplo
```cpp


FILE_BASIC_INFO basicInfo;
    BOOL result;

    result = GetFileInformationByHandleEx( hFile,
                                               FileBasicInfo,
                                               &basicInfo,
                                               sizeof(basicInfo));

\\...

printf("  File Attributes: ");
    PrintFileAttributes(basicInfo.FileAttributes);

\\...
VOID
PrintFileAttributes(
    ULONG FileAttributes
    )
{
    
    if (FileAttributes & FILE_ATTRIBUTE_ARCHIVE) {
        printf("Archive ");
    }
    if (FileAttributes & FILE_ATTRIBUTE_DIRECTORY) {
        printf("Directory ");
    }
    if (FileAttributes & FILE_ATTRIBUTE_READONLY) {
        printf("Read-Only ");
    }
}
```

Exemplo obtido de um [exemplo clássico do Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/io/extendedfileapis/ExtendedFileAPIs.cpp) no github.



| Constante/valor                                                                                                                                                                                                                                                                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILE_ATTRIBUTE_ARCHIVE"></span><span id="file_attribute_archive"></span><dl> Do <dt>**arquivo \_ \_Arquivo de atributo**</dt> <dt>32 (0x20)</dt> </dl>                                                       | Um arquivo ou diretório que é um arquivo ou diretório morto. Normalmente, os aplicativos usam esse atributo para marcar arquivos para backup ou remoção. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="FILE_ATTRIBUTE_COMPRESSED"></span><span id="file_attribute_compressed"></span><dl> Do <dt>**arquivo \_ ATRIBUTO \_ compactado**</dt> <dt>2048 (0x800)</dt> </dl>                                           | Um arquivo ou diretório que é compactado. Para um arquivo, todos os dados no arquivo são compactados. Para um diretório, a compactação é o padrão para arquivos e subdiretórios recém-criados.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="FILE_ATTRIBUTE_DEVICE"></span><span id="file_attribute_device"></span><dl> Do <dt>**arquivo \_ \_Dispositivo de atributo**</dt> <dt>64 (0x40)</dt> </dl>                                                          | Esse valor é reservado para uso do sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="FILE_ATTRIBUTE_DIRECTORY"></span><span id="file_attribute_directory"></span><dl> Do <dt>**arquivo \_ \_Diretório de atributo**</dt> <dt>16 (0x10)</dt> </dl>                                                 | O identificador que identifica um diretório.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="FILE_ATTRIBUTE_ENCRYPTED"></span><span id="file_attribute_encrypted"></span><dl> Do <dt>**arquivo \_ ATRIBUTO \_ ENCRYPTED**</dt> <dt>16384 (0x4000)</dt> </dl>                                            | Um arquivo ou diretório que é criptografado. Para um arquivo, todos os fluxos de dados no arquivo são criptografados. Para um diretório, a criptografia é o padrão para arquivos e subdiretórios recém-criados.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ATTRIBUTE_HIDDEN"></span><span id="file_attribute_hidden"></span><dl> Do <dt>**arquivo \_ ATRIBUTO \_ Hidden**</dt> <dt>2 (0x2)</dt> </dl>                                                            | O arquivo ou diretório está oculto. Ele não está incluído em uma listagem de diretório comum.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ATTRIBUTE_INTEGRITY_STREAM"></span><span id="file_attribute_integrity_stream"></span><dl> Do <dt>**arquivo \_ \_ \_ Fluxo de integridade de atributo**</dt> <dt>32768 (0x8000)</dt> </dl>                      | O fluxo de dados do diretório ou do usuário é configurado com integridade (somente com suporte em volumes ReFS). Ele não está incluído em uma listagem de diretório comum. A configuração de integridade persiste com o arquivo se ele for renomeado. Se um arquivo for copiado, o arquivo de destino terá a integridade definida se o arquivo de origem ou o diretório de destino tiver a integridade definida.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para esse sinalizador até o Windows Server 2012.<br/>                              |
| <span id="FILE_ATTRIBUTE_NORMAL"></span><span id="file_attribute_normal"></span><dl> Do <dt>**arquivo \_ ATRIBUTO \_ NORMAL**</dt> <dt>128 (0x80)</dt> </dl>                                                         | Um arquivo que não tem outros atributos definidos. Esse atributo é válido somente quando usado sozinho.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="FILE_ATTRIBUTE_NOT_CONTENT_INDEXED"></span><span id="file_attribute_not_content_indexed"></span><dl> Do <dt>**arquivo \_ ATRIBUTO \_ sem \_ conteúdo \_ indexado**</dt> <dt>8192 (0x2000)</dt> </dl>             | O arquivo ou diretório não deve ser indexado pelo serviço de indexação de conteúdo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="FILE_ATTRIBUTE_NO_SCRUB_DATA"></span><span id="file_attribute_no_scrub_data"></span><dl> Do <dt>**arquivo \_ ATRIBUTO \_ sem \_ \_ dados de limpeza**</dt> <dt>131072 (0x20000)</dt> </dl>                            | O fluxo de dados do usuário não deve ser lido pelo verificador de integridade de dados em segundo plano (também conhecido como scrubbing). Quando definido em um diretório, ele só fornece herança. Esse sinalizador só tem suporte em espaços de armazenamento e volumes ReFS. Ele não está incluído em uma listagem de diretório comum.<br/> **Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para esse sinalizador até o Windows 8 e o Windows Server 2012.<br/>                                                                                                    |
| <span id="FILE_ATTRIBUTE_OFFLINE"></span><span id="file_attribute_offline"></span><dl> Do <dt>**arquivo \_ ATRIBUTO \_ OFFLINE**</dt> <dt>4096 (0x1000)</dt> </dl>                                                   | Os dados de um arquivo não estão disponíveis imediatamente. Esse atributo indica que os dados de arquivo são movidos fisicamente para o armazenamento offline. Esse atributo é usado pelo armazenamento remoto, que é o software de gerenciamento de armazenamento hierárquico. Os aplicativos não devem alterar arbitrariamente esse atributo.<br/>                                                                                                                                                                                                                                                                         |
| <span id="FILE_ATTRIBUTE_READONLY"></span><span id="file_attribute_readonly"></span><dl> Do <dt>**arquivo \_ ATRIBUTO \_ ReadOnly**</dt> <dt>1 (0x1)</dt> </dl>                                                      | Um arquivo que é somente leitura. Os aplicativos podem ler o arquivo, mas não podem gravar nele nem excluí-lo. Esse atributo não é respeitado em diretórios. Para obter mais informações, consulte [você não pode exibir ou alterar os atributos de sistema somente leitura ou de pastas no Windows Server 2003, no Windows XP, no Windows Vista ou no Windows 7](https://support.microsoft.com/kb/326549).<br/>                                                                                                                                                                                           |
| <span id="FILE_ATTRIBUTE_RECALL_ON_DATA_ACCESS"></span><span id="file_attribute_recall_on_data_access"></span><dl> Do <dt>**arquivo \_ \_Cancelamento \_ de atributo no \_ \_ acesso a dados**</dt> <dt>4194304 (0x400000)</dt> </dl> | Quando esse atributo é definido, isso significa que o arquivo ou diretório não está totalmente presente localmente. Para um arquivo que significa que nem todos os seus dados estão no armazenamento local (por exemplo, pode ser esparso com alguns dados ainda no armazenamento remoto). Para um diretório, isso significa que alguns dos conteúdos de diretório estão sendo virtualizados de outro local. Ler o arquivo/enumerar o diretório será mais caro do que o normal, por exemplo, fará com que pelo menos um conteúdo de arquivo/diretório seja buscado em um repositório remoto. Somente os chamadores de modo kernel podem definir esse bit.<br/> |
| <span id="FILE_ATTRIBUTE_RECALL_ON_OPEN"></span><span id="file_attribute_recall_on_open"></span><dl> Do <dt>**arquivo \_ \_Cancelamento \_ de atributo na \_ abertura**</dt> <dt>262144 (0x40000)</dt> </dl>                         | Esse atributo só aparece em classes de enumeração de diretório \_ ( \_ informações de diretório de arquivo, informações de dir de arquivo \_ \_ \_ , etc.). Quando esse atributo é definido, isso significa que o arquivo ou diretório não tem nenhuma representação física no sistema local; o item é virtual. Abrir o item será mais caro do que o normal, por exemplo, fará com que pelo menos um deles seja obtido de um repositório remoto.<br/>                                                                                                                                                                 |
| <span id="FILE_ATTRIBUTE_REPARSE_POINT"></span><span id="file_attribute_reparse_point"></span><dl> Do <dt>**arquivo \_ \_ \_ Ponto de nova análise de atributo**</dt> <dt>1024 (0x400)</dt> </dl>                                 | Um arquivo ou diretório que tem um ponto de nova análise associado ou um arquivo que é um link simbólico.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FILE_ATTRIBUTE_SPARSE_FILE"></span><span id="file_attribute_sparse_file"></span><dl> Do <dt>**arquivo \_ \_ \_ Arquivo ESPARSO do atributo**</dt> <dt>512 (0x200)</dt> </dl>                                        | Um arquivo que é um arquivo esparso.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="FILE_ATTRIBUTE_SYSTEM"></span><span id="file_attribute_system"></span><dl> Do <dt>**arquivo \_ \_Sistema de atributos**</dt> <dt>4 (0x4)</dt> </dl>                                                            | Um arquivo ou diretório do qual o sistema operacional usa uma parte ou usa exclusivamente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="FILE_ATTRIBUTE_TEMPORARY"></span><span id="file_attribute_temporary"></span><dl> Do <dt>**arquivo \_ ATRIBUTO \_ temporário**</dt> <dt>256 (0x100)</dt> </dl>                                               | Um arquivo que está sendo usado para armazenamento temporário. Os sistemas de arquivos evitam gravar dados de volta no armazenamento em massa se houver memória de cache suficiente disponível, porque normalmente, um aplicativo exclui um arquivo temporário depois que o identificador é fechado. Nesse cenário, o sistema pode evitar totalmente a gravação dos dados. Caso contrário, os dados serão gravados depois que o identificador for fechado.<br/>                                                                                                                                                                                                       |
| <span id="FILE_ATTRIBUTE_VIRTUAL"></span><span id="file_attribute_virtual"></span><dl> Do <dt>**arquivo \_ ATRIBUTO \_ VIRTUAL**</dt> <dt>65536 (0x10000)</dt> </dl>                                                 | Esse valor é reservado para uso do sistema.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>WinNT. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributo de compactação](compression-attribute.md)
</dt> <dt>

[Criando e abrindo arquivos](creating-and-opening-files.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda)
</dt> <dt>

[**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle)
</dt> <dt>

[**GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex)
</dt> <dt>

[**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[**SetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda)
</dt> <dt>

[**SetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle)
</dt> </dl>

 

 




