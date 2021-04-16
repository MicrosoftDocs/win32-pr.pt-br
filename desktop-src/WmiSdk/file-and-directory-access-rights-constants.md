---
description: As classes WMI que representam arquivos ou diretórios, como o arquivo de codec do Win32 filefile \_ ou CIM \_ , contêm uma propriedade AccessMask.
ms.assetid: 9020b337-d44f-4247-b623-68a1bcf35abb
ms.tgt_platform: multiple
title: Constantes de direitos de acesso de arquivo e diretório (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c0ddca31034ffde79fa9d9ff902a364cf07e311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105773029"
---
# <a name="file-and-directory-access-rights-constants"></a>Constantes de direitos de acesso de arquivo e diretório

As classes WMI que representam arquivos ou diretórios, como o [**\_ arquivo**](/windows/desktop/CIMWin32Prov/cim-datafile)de [**\_ codec do Win32**](/windows/desktop/CIMWin32Prov/win32-codecfile) filefile ou CIM, contêm uma propriedade **AccessMask** . Essa propriedade contém configurações de bit que especificam os direitos de acesso que um usuário ou grupo deve ter para acessar ou operações específicas no arquivo. Para obter mais informações, consulte [segurança de arquivos e direitos de acesso](/windows/desktop/FileIO/file-security-and-access-rights) e [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).

As classes de arquivo ou diretório que contêm uma propriedade **AccessMask** incluem:

-   [**DataFile de CIM \_**](/windows/desktop/CIMWin32Prov/cim-datafile)
-   [**\_Diretório CIM**](/windows/desktop/CIMWin32Prov/cim-directory)
-   [**CIM \_ LogicalFile**](/windows/desktop/CIMWin32Prov/cim-logicalfile)
-   [**Codec do Win32 \_**](/windows/desktop/CIMWin32Prov/win32-codecfile)
-   [**\_Diretório Win32**](/windows/desktop/CIMWin32Prov/win32-directory)
-   [**\_NTEventLogFile Win32**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))
-   [**Compartilhamento do Win32 \_**](/windows/desktop/CIMWin32Prov/win32-share)
-   [**Atalho do Win32 \_**](/windows/desktop/CIMWin32Prov/win32-shortcutfile)

A lista a seguir lista os valores para direitos de acesso de arquivo e diretório na propriedade **AccessMask** . Esta propriedade é um bitmap.

<dl> <dt>

<span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**\_dados de leitura de arquivo \_**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Concede o direito de ler dados do arquivo.


</dt> </dl> </dd> <dt>

<span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**\_diretório de lista de arquivos \_**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Concede o direito de ler dados do arquivo. Para um diretório, esse valor concede o direito de listar o conteúdo do diretório.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**\_dados de gravação de arquivo \_**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Concede o direito de gravar dados no arquivo.


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**ARQUIVO- \_ Adicionar \_ arquivo**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Concede o direito de gravar dados no arquivo. Para um diretório, esse valor concede o direito de criar um arquivo no diretório.


</dt> </dl> </dd> <dt>

<span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**\_dados de acréscimo de arquivo \_**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Concede o direito de acrescentar dados ao arquivo. Para um diretório, esse valor concede o direito de criar um subdiretório.


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**ARQUIVO \_ Adicionar \_ subdiretório**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Concede o direito de acrescentar dados ao arquivo. Para um diretório, esse valor concede o direito de criar um subdiretório.


</dt> </dl> </dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**ARQUIVO de \_ leitura \_ ea**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Concede o direito de ler atributos estendidos.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**\_ea de gravação de arquivo \_**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Concede o direito de gravar atributos estendidos.


</dt> </dl> </dd> <dt>

<span id="FILE_EXECUTE"></span><span id="file_execute"></span>**\_Executar arquivo**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Concede o direito de executar um arquivo.


</dt> </dl> </dd> <dt>

<span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**\_atravessamento de arquivo**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Concede o direito de executar um arquivo. Para um diretório, o diretório pode ser atravessado.


</dt> </dl> </dd> <dt>

<span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**\_excluir arquivo \_ filho**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Concede o direito de excluir um diretório e todos os arquivos que ele contém (seus filhos), mesmo que os arquivos sejam somente leitura.


</dt> </dl> </dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**\_atributos de leitura de arquivo \_**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Concede o direito de ler atributos de arquivo.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**\_atributos de gravação de arquivo \_**
</dt> <dd> <dl> <dt>

256 (0x100)
</dt> <dt>



Concede o direito de alterar atributos de arquivo.


</dt> </dl> </dd> <dt>

<span id="DELETE"></span><span id="delete"></span>**APAGAR**
</dt> <dd> <dl> <dt>

65536 (0x10000)
</dt> <dt>



Concede o direito de excluir o objeto.


</dt> </dl> </dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>**controle de leitura \_**
</dt> <dd> <dl> <dt>

131072 (0x20000)
</dt> <dt>



Concede o direito de ler as informações no descritor de segurança do objeto, sem incluir as informações na SACL.


</dt> </dl> </dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**GRAVAR \_ DAC**
</dt> <dd> <dl> <dt>

262144 (0x40000)
</dt> <dt>



Concede o direito de modificar a DACL no descritor de segurança do objeto para o objeto.


</dt> </dl> </dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**proprietário da gravação \_**
</dt> <dd> <dl> <dt>

524288 (0x80000)
</dt> <dt>



Concede o direito de alterar o proprietário no descritor de segurança do objeto.


</dt> </dl> </dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**NOVAMENTE**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



Concede o direito de usar o objeto para sincronização. Isso permite que um processo aguarde até que o objeto esteja no estado sinalizado. Alguns tipos de objeto não dão suporte a esse direito de acesso.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Winnt. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de segurança do WMI](wmi-security-constants.md)
</dt> <dt>

[Mantendo a segurança do WMI](maintaining-wmi-security.md)
</dt> </dl>

 

