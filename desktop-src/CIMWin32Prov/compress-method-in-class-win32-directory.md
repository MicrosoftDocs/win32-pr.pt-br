---
description: Compacta o arquivo de entrada de diretório lógico (ou diretório) especificado no caminho do objeto.
ms.assetid: 4db13622-75c5-45db-8536-451059c0e477
ms.tgt_platform: multiple
title: Método compress da classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea694c09e11e5801016a4ea85b9774448c542991
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088977"
---
# <a name="compress-method-of-the-win32_directory-class"></a>Método compress da classe do \_ diretório Win32

O método **compactar** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) compacta o arquivo de entrada de diretório lógico (ou diretório) especificado no caminho do objeto.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Compress();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor de 0 (zero) se o arquivo tiver sido compactado com êxito e qualquer outro número para indicar um erro.

<dl> <dt>

**0**
</dt> <dd>

A solicitação foi bem-sucedida.

</dd> <dt>

**2**
</dt> <dd>

Acesso negado.

</dd> <dt>

**8**
</dt> <dd>

Ocorreu uma falha não especificada.

</dd> <dt>

**9**
</dt> <dd>

O nome especificado não era válido.

</dd> <dt>

**10**
</dt> <dd>

O objeto especificado já existe.

</dd> <dt>

**11**
</dt> <dd>

O sistema de arquivos não é um NTFS.

</dd> <dt>

**12**
</dt> <dd>

A plataforma não é o Windows.

</dd> <dt>

**13**
</dt> <dd>

A unidade não é a mesma.

</dd> <dt>

**14**
</dt> <dd>

O diretório não está vazio.

</dd> <dt>

**15**
</dt> <dd>

Houve uma violação de compartilhamento.

</dd> <dt>

**16**
</dt> <dd>

O arquivo de inicialização especificado não era válido.

</dd> <dt>

**17**
</dt> <dd>

Um privilégio necessário para a operação não é mantido.

</dd> <dt>

**Abril**
</dt> <dd>

Um parâmetro especificado não é válido.

</dd> </dl>

## <a name="remarks"></a>Comentários

A compactação fornece uma maneira de liberar espaço de armazenamento adicional em uma unidade de disco sem comprar novo hardware e sem remover arquivos ou pastas. Dependendo do tamanho do disco rígido e do tipo de arquivos armazenados nesse disco, você poderá recuperar centenas de megabytes de espaço em disco e, portanto, impedir a necessidade de comprar um novo disco rígido e colocar o computador offline até que a nova unidade seja instalada.

O método compress compacta todos os arquivos e subpastas dentro de uma pasta especificada. Além disso, a classe também inclui um método descompactar que remove a compactação de todos os arquivos e subpastas em uma pasta. Métodos semelhantes também são fornecidos com a classe de DataFile do CIM \_ . Isso permite que você compacte ou Descompacte seletivamente arquivos específicos dentro de uma pasta.

Como a compactação faz uma ligeira penalidade de desempenho, não é recomendável para arquivos ou pastas que são acessados rotineiramente; por exemplo, você provavelmente não deseja compactar arquivos de banco de dados, arquivos de log ou pastas de perfil de usuário. Melhores candidatos para compactação são arquivos e pastas que não são acessados com muita frequência. Por exemplo, você pode escrever um script para retornar uma coleção de pastas em uma unidade que não foi acessada por um mês ou mais e, em seguida, compactar cada uma dessas pastas.

A quantidade de espaço em disco liberada pela compactação de pastas varia dependendo do tipo de arquivos armazenados nessa pasta. Por exemplo, arquivos. jpg já estão compactados e a compactação adicional tem pouco efeito sobre o tamanho do arquivo. No entanto, com outros tipos de arquivo, a economia pode ser considerável. Por exemplo, uma nova pasta foi criada em um computador de teste baseado no Windows 2000 e os documentos 33 do Microsoft Word, ocupando um total de 15 megabytes (MB) de espaço em disco, foram copiados nessa pasta. Quando os documentos foram compactados, a pasta demorou apenas 7 MB de espaço em disco.

## <a name="examples"></a>Exemplos

O exemplo de VBScript a seguir compacta a pasta C: \\ scripts.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Compress
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Diretório Win32**](win32-directory.md)
</dt> <dt>

[**Descompactar**](uncompress-method-in-class-win32-directory.md)
</dt> </dl>

 

