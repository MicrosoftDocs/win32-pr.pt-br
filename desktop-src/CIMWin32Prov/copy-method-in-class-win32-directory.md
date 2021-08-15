---
description: Copia o arquivo de entrada de diretório lógico ou o diretório especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.
ms.assetid: 038e23d7-71db-4db6-8fb1-e84e972510c9
ms.tgt_platform: multiple
title: Método Copy da classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 85a16d3e63ef46ad2c536103a4e462a3e830e17f56f83cdcf39bbad5a33ebb23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118419751"
---
# <a name="copy-method-of-the-win32_directory-class"></a>Método Copy da classe do \_ diretório Win32

O método **Copy** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) copia o arquivo de entrada de diretório lógico ou o diretório especificado no caminho do objeto para o local especificado pelo parâmetro de entrada. Não haverá suporte para uma cópia se a substituição de um arquivo lógico existente for necessária.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Copy(
   string FileName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FileName* 
</dt> <dd>

Nome totalmente qualificado da cópia do arquivo (ou diretório). Exemplo: c: \\ temp \\ newdirectory

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 (zero) se o arquivo foi copiado com êxito e qualquer outro número para indicar um erro.

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

O sistema de arquivos não é NTFS.

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

As pastas geralmente precisam ser copiadas de um local para outro. Por exemplo, você pode copiar uma pasta de um servidor para outro para criar uma cópia de backup dessa pasta. Ou você pode ter uma pasta de modelos que precisa ser copiada para estações de trabalho de usuário ou uma pasta de scripts que deve ser copiada para todos os seus servidores DNS.

O método de cópia de diretório do Win32 \_ permite que você copie uma pasta de um local para outro, no mesmo computador (por exemplo, copiando uma pasta da unidade C para a unidade D) ou em um computador remoto. Para copiar uma pasta, você retorna uma instância da pasta a ser copiada e, em seguida, chama o método Copy, passando como um parâmetro o local de destino para a nova cópia da pasta. Por exemplo, esta linha de código copia uma pasta para a pasta scripts na unidade F:

`objFolder.Copy("F:\Scripts")`

O WMI não substituirá uma pasta existente ao executar o método de cópia. Isso significa que a operação de cópia falhará se a pasta de destino existir. Por exemplo, suponha que você tenha uma pasta chamada scripts e tente copiar essa pasta para um compartilhamento remoto denominado \\ \\ ATL-FS-01 \\ Archive. Se uma pasta denominada scripts já existir nesse compartilhamento, a operação de cópia falhará.

## <a name="examples"></a>Exemplos

O exemplo de código opções, extraído da [pasta Copy a usando o WMI](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2), usa o método Copy para copiar a pasta C: \\ scripts para D: \\ Archive.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery( _ 
    "Select * from Win32_Directory where Name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults  = objFolder.Copy("D:\Archive") 
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
</dt> </dl>

 

