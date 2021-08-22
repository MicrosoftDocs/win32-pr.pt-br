---
description: As classes WMI que representam arquivos ou diretórios, como Win32 \_ CodecFile ou CIM \_ DataFile, contêm uma propriedade AccessMask.
ms.assetid: 9020b337-d44f-4247-b623-68a1bcf35abb
ms.tgt_platform: multiple
title: Constantes de direitos de acesso de arquivo e diretório (Winnt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8678627b0f7d9ce2ed7f9c8e7e39c49bdcd3b6c3a8313f7d7b3c517c379093d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131378"
---
# <a name="file-and-directory-access-rights-constants"></a>Constantes de direitos de acesso de arquivo e diretório

As classes WMI que representam arquivos ou diretórios, como [**Win32 \_ CodecFile**](/windows/desktop/CIMWin32Prov/win32-codecfile) ou [**CIM \_ DataFile,**](/windows/desktop/CIMWin32Prov/cim-datafile)contêm uma **propriedade AccessMask.** Essa propriedade contém configurações de bit que especificam os direitos de acesso que um usuário ou grupo deve ter para acesso específico ou operações no arquivo. Para obter mais informações, consulte [Segurança de arquivos e direitos de acesso](/windows/desktop/FileIO/file-security-and-access-rights) e Alterando a segurança de acesso em objetos [securáveis.](changing-access-security-on-securable-objects.md)

As classes de arquivo ou diretório que contêm uma **propriedade AccessMask** incluem:

-   [**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile)
-   [**Diretório \_ CIM**](/windows/desktop/CIMWin32Prov/cim-directory)
-   [**CIM \_ LogicalFile**](/windows/desktop/CIMWin32Prov/cim-logicalfile)
-   [**CodecFile do Win32 \_**](/windows/desktop/CIMWin32Prov/win32-codecfile)
-   [**Diretório \_ Win32**](/windows/desktop/CIMWin32Prov/win32-directory)
-   [**Win32 \_ NTEventLogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))
-   [**Compartilhamento \_ win32**](/windows/desktop/CIMWin32Prov/win32-share)
-   [**Win32 \_ ShortcutFile**](/windows/desktop/CIMWin32Prov/win32-shortcutfile)

A lista a seguir lista os valores para direitos de acesso de arquivo e diretório na **propriedade AccessMask.** Essa propriedade é um bitmap.

<dl> <dt>

<span id="FILE_READ_DATA"></span><span id="file_read_data"></span>**DADOS \_ DE LEITURA DE \_ ARQUIVO**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Concede o direito de ler dados do arquivo.


</dt> </dl> </dd> <dt>

<span id="FILE_LIST_DIRECTORY"></span><span id="file_list_directory"></span>**DIRETÓRIO DE \_ LISTA DE \_ ARQUIVOS**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Concede o direito de ler dados do arquivo. Para um diretório, esse valor concede o direito de listar o conteúdo do diretório.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_DATA"></span><span id="file_write_data"></span>**DADOS DE \_ GRAVAÇÃO DE \_ ARQUIVO**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Concede o direito de gravar dados no arquivo.


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_FILE"></span><span id="file_add_file"></span>**FILE \_ ADD \_ FILE**
</dt> <dd> <dl> <dt>

2 (0x2)
</dt> <dt>



Concede o direito de gravar dados no arquivo. Para um diretório, esse valor concede o direito de criar um arquivo no diretório .


</dt> </dl> </dd> <dt>

<span id="FILE_APPEND_DATA"></span><span id="file_append_data"></span>**ARQUIVO \_ ANEXAR \_ DADOS**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Concede o direito de anexar dados ao arquivo. Para um diretório, esse valor concede o direito de criar um subdiretório.


</dt> </dl> </dd> <dt>

<span id="FILE_ADD_SUBDIRECTORY"></span><span id="file_add_subdirectory"></span>**FILE \_ ADD \_ SUBDIRECTORY**
</dt> <dd> <dl> <dt>

4 (0x4)
</dt> <dt>



Concede o direito de anexar dados ao arquivo. Para um diretório, esse valor concede o direito de criar um subdiretório.


</dt> </dl> </dd> <dt>

<span id="FILE_READ_EA"></span><span id="file_read_ea"></span>**EA \_ DE \_ LEITURA DE ARQUIVO**
</dt> <dd> <dl> <dt>

8 (0x8)
</dt> <dt>



Concede o direito de ler atributos estendidos.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_EA"></span><span id="file_write_ea"></span>**EA \_ DE \_ GRAVAÇÃO DE ARQUIVO**
</dt> <dd> <dl> <dt>

16 (0x10)
</dt> <dt>



Concede o direito de gravar atributos estendidos.


</dt> </dl> </dd> <dt>

<span id="FILE_EXECUTE"></span><span id="file_execute"></span>**FILE \_ EXECUTE**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Concede o direito de executar um arquivo.


</dt> </dl> </dd> <dt>

<span id="FILE_TRAVERSE"></span><span id="file_traverse"></span>**CAMINHO \_ DO ARQUIVO**
</dt> <dd> <dl> <dt>

32 (0x20)
</dt> <dt>



Concede o direito de executar um arquivo. Para um diretório, o diretório pode ser percorrido.


</dt> </dl> </dd> <dt>

<span id="FILE_DELETE_CHILD"></span><span id="file_delete_child"></span>**FILHO \_ DE EXCLUSÃO \_ DE ARQUIVO**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Concede o direito de excluir um diretório e todos os arquivos que ele contém (seus filhos), mesmo que os arquivos sejam somente leitura.


</dt> </dl> </dd> <dt>

<span id="FILE_READ_ATTRIBUTES"></span><span id="file_read_attributes"></span>**ATRIBUTOS \_ DE LEITURA DE \_ ARQUIVO**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Concede o direito de ler atributos de arquivo.


</dt> </dl> </dd> <dt>

<span id="FILE_WRITE_ATTRIBUTES"></span><span id="file_write_attributes"></span>**ATRIBUTOS DE \_ GRAVAÇÃO \_ DE ARQUIVO**
</dt> <dd> <dl> <dt>

256 (0x100)
</dt> <dt>



Concede o direito de alterar atributos de arquivo.


</dt> </dl> </dd> <dt>

<span id="DELETE"></span><span id="delete"></span>**Excluir**
</dt> <dd> <dl> <dt>

65536 (0x10000)
</dt> <dt>



Concede o direito de excluir o objeto .


</dt> </dl> </dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>**CONTROLE \_ DE LEITURA**
</dt> <dd> <dl> <dt>

131072 (0x20000)
</dt> <dt>



Concede o direito de ler as informações no descritor de segurança do objeto, não incluindo as informações na SACL.


</dt> </dl> </dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>**ESCREVER \_ DAC**
</dt> <dd> <dl> <dt>

262144 (0x40000)
</dt> <dt>



Concede o direito de modificar a DACL no descritor de segurança do objeto para o objeto .


</dt> </dl> </dd> <dt>

<span id="WRITE_OWNER"></span><span id="write_owner"></span>**PROPRIETÁRIO \_ DA GRAVAÇÃO**
</dt> <dd> <dl> <dt>

524288 (0x80000)
</dt> <dt>



Concede o direito de alterar o proprietário no descritor de segurança do objeto.


</dt> </dl> </dd> <dt>

<span id="SYNCHRONIZE"></span><span id="synchronize"></span>**Sincronizar**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



Concede o direito de usar o objeto para sincronização. Isso permite que um processo aguarde até que o objeto está no estado sinalizado. Alguns tipos de objeto não suportam esse direito de acesso.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Winnt.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes de segurança WMI](wmi-security-constants.md)
</dt> <dt>

[Mantendo a segurança WMI](maintaining-wmi-security.md)
</dt> </dl>

 

