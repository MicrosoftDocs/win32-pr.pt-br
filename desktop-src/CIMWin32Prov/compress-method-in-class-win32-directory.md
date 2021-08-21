---
description: Compacta o arquivo de entrada de diretório lógico (ou diretório) especificado no caminho do objeto.
ms.assetid: 4db13622-75c5-45db-8536-451059c0e477
ms.tgt_platform: multiple
title: Método compactar da classe Win32_Directory classe
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
ms.openlocfilehash: 15d9142abb95998fce803c30c439632775cd8ff807f3b7d99653875d08e534e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020664"
---
# <a name="compress-method-of-the-win32_directory-class"></a>Método Compactar da classe De diretório \_ Win32

O **método de** classe [Compress WMI](/windows/desktop/WmiSdk/retrieving-a-class) compacta o arquivo de entrada de diretório lógico (ou diretório) especificado no caminho do objeto.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Compress();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará um valor de 0 (zero) se o arquivo tiver sido compactado com êxito e qualquer outro número para indicar um erro.

<dl> <dt>

**0**
</dt> <dd>

A solicitação foi bem-sucedida.

</dd> <dt>

**2**
</dt> <dd>

O acesso foi negado.

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

A plataforma não é Windows.

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

O arquivo inicial especificado não era válido.

</dd> <dt>

**17**
</dt> <dd>

Um privilégio necessário para a operação não é mantido.

</dd> <dt>

**21**
</dt> <dd>

Um parâmetro especificado não é válido.

</dd> </dl>

## <a name="remarks"></a>Comentários

A compactação fornece uma maneira de liberar espaço de armazenamento adicional em uma unidade de disco sem comprar um novo hardware e sem remover arquivos ou pastas. Dependendo do tamanho do disco rígido e do tipo de arquivos armazenados nesse disco, você poderá recuperar centenas de megabytes de espaço em disco e, portanto, impedir a necessidade de comprar um novo disco rígido e colocar o computador offline até que a nova unidade seja instalada.

O método Compress compacta todos os arquivos e subpastas dentro de uma pasta especificada. Além disso, a classe também inclui um método Uncompress que remove a compactação de todos os arquivos e subpastas em uma pasta. Métodos semelhantes também são fornecidos com a classe Cim \_ Datafile. Isso permite compactar ou descompactar seletivamente arquivos específicos dentro de uma pasta.

Como a compactação transmite uma pequena penalidade de desempenho, não é recomendável para arquivos ou pastas que são acessados de forma rotineira; por exemplo, você provavelmente não deseja compactar arquivos de banco de dados, arquivos de log ou pastas de perfil de usuário. Melhores candidatos para compactação são arquivos e pastas que não são acessados com muita frequência. Por exemplo, você pode escrever um script para retornar uma coleção de pastas em uma unidade que não foi acessada por um mês ou mais e compactar cada uma dessas pastas.

A quantidade de espaço em disco liberada pela compactação de pastas varia dependendo do tipo de arquivos armazenados nessa pasta. Por exemplo, .jpg arquivos já estão compactados e a compactação posterior tem pouco efeito no tamanho do arquivo. No entanto, com outros tipos de arquivo, a economia pode ser considerável. Por exemplo, uma nova pasta foi criada em um computador de teste baseado em Windows 2000 e 33 documentos Microsoft Word, ocupando um total de 15 MB (megabytes) de espaço em disco, foram copiados para essa pasta. Quando os documentos foram compactados, a pasta tinha apenas 7 MB de espaço em disco.

## <a name="examples"></a>Exemplos

O exemplo de VBScript a seguir compacta a pasta C: \\ Scripts.


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
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Diretório \_ Win32**](win32-directory.md)
</dt> <dt>

[**Descompactar**](uncompress-method-in-class-win32-directory.md)
</dt> </dl>

 

