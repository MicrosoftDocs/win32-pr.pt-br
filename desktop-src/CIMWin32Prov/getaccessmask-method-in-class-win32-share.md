---
description: Método GetAccessMask da classe Win32_Share – retorna um bitmap UInt32 com os direitos de acesso ao compartilhamento mantido pelo usuário ou grupo em cujo nome a instância é retornada.
ms.assetid: 234f44a4-ffff-431d-a973-98f2bd313c7d
ms.tgt_platform: multiple
title: Método GetAccessMask da classe Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.GetAccessMask
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fcd6396f6421060a67108e7c428c99bcd7ca9651
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097014"
---
# <a name="getaccessmask-method-of-the-win32_share-class"></a>Método GetAccessMask da classe de \_ compartilhamento do Win32

O método **GetAccessMask** retorna um bitmap UInt32 com os direitos de acesso ao compartilhamento mantido pelo usuário ou grupo em cujo nome a instância é retornada.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Direitos de acesso ao compartilhamento mantido pelo usuário ou grupo.

<dl> <dt>

**\_diretório de lista de arquivos \_**
</dt> <dd>

1 (0x1)

Concede o direito de ler dados do arquivo. Para um diretório, esse valor concede o direito de listar o conteúdo do diretório.

</dd> <dt>

**ARQUIVO- \_ Adicionar \_ arquivo**
</dt> <dd>

2 (0x2)

Concede o direito de gravar dados no arquivo. Para um diretório, esse valor concede o direito de criar um arquivo no diretório.

</dd> <dt>

**ARQUIVO \_ Adicionar \_ subdiretório**
</dt> <dd>

4 (0x4)

Concede o direito de acrescentar dados ao arquivo. Para um diretório, esse valor concede o direito de criar um subdiretório.

</dd> <dt>

**ARQUIVO de \_ leitura \_ ea**
</dt> <dd>

8 (0x8)

Concede o direito de ler atributos estendidos.

</dd> <dt>

**\_ea de gravação de arquivo \_**
</dt> <dd>

16 (0x10)

Concede o direito de gravar atributos estendidos.

</dd> <dt>

**\_atravessamento de arquivo**
</dt> <dd>

32 (0x20)

Concede o direito de executar um arquivo. Para um diretório, o diretório pode ser atravessado.

</dd> <dt>

**\_excluir arquivo \_ filho**
</dt> <dd>

64 (0x40)

Concede o direito de excluir um diretório e todos os arquivos que ele contém (seus filhos), mesmo que os arquivos sejam somente leitura.

</dd> <dt>

**\_atributos de leitura de arquivo \_**
</dt> <dd>

128 (0x80)

Concede o direito de ler atributos de arquivo.

</dd> <dt>

**\_atributos de gravação de arquivo \_**
</dt> <dd>

256 (0x100)

Concede o direito de alterar atributos de arquivo.

</dd> <dt>

**DELETE**
</dt> <dd>

65536 (0x10000)

Concede acesso de exclusão.

</dd> <dt>

**controle de leitura \_**
</dt> <dd>

131072 (0x20000)

Concede acesso de leitura ao descritor de segurança e ao proprietário.

</dd> <dt>

**GRAVAR \_ DAC**
</dt> <dd>

262144 (0x40000)

Concede acesso de gravação à DACL (lista de controle de acesso discricionário).

</dd> <dt>

**proprietário da gravação \_**
</dt> <dd>

524288 (0x80000)

Atribui o proprietário da gravação.

</dd> <dt>

**SYNCHRONIZE**
</dt> <dd>

1048576 (0x100000)

Sincroniza o acesso e permite que um processo Aguarde um objeto para entrar no estado sinalizado.

</dd> </dl>

## <a name="remarks"></a>Comentários

O método **GetAccessMask** é um método de objeto e é usado em uma ocorrência dessa classe.

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir cria uma pasta de compartilhamento e Obtém o valor da máscara de acesso no descritor de segurança que protege a pasta de compartilhamento.


```VB
Const FILE_SHARE = 0
Const MAXIMUM_CONNECTIONS = 4000 
strComputer = "."

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objNewShare = objWMIService.Get("Win32_Share")
Return = objNewShare.Create ("C:\Temp", "TestShare", FILE_SHARE, MAXIMUM_CONNECTIONS, "test share")

If Return <> 0 Then
          WScript.Echo Return
          WScript.Quit
End If

Set objShare = objWMIService.Get("Win32_Share.Name='TestShare'")
Return = objShare.GetAccessMask
WScript.Echo Return
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Compartilhamento do Win32 \_**](win32-share.md)
</dt> </dl>

 

