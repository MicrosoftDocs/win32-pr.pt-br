---
description: Renomeia o arquivo de entrada de diretório especificado no caminho do objeto.
ms.assetid: 8bfe1b69-5f93-4408-a742-f03a9cb16bfe
ms.tgt_platform: multiple
title: Renomear o método da Win32_Directory classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 86b6bd35b14ee2a342dee27615c1ff21d9274a5f3020c4f804df5065f430813f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077436"
---
# <a name="rename-method-of-the-win32_directory-class"></a>Renomear o método da classe De diretório \_ Win32

O **método renomear** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) renomeia o arquivo de entrada de diretório especificado no caminho do objeto. Não há suporte para renomeação se o destino estiver em outra unidade ou se for necessário sobrescrever um arquivo lógico existente.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Rename(
   string FileName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FileName* 
</dt> <dd>

Nome totalmente qualificado do arquivo (ou diretório). Exemplo: c: \\ temp \\newfile.txt.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará um valor de 0 (zero) se o arquivo tiver sido renomeado com êxito e qualquer outro número para indicar um erro.

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

Para renomear uma pasta, primeiro a bind à pasta em questão e, em seguida, chame o método Renomear. Como o único parâmetro para o método , passe o novo nome para a pasta como um nome de caminho completo. Por exemplo, se a pasta no Backup de Logs de Scripts C: for renomeada C: Arquivo de Scripts, você deverá passar \\ \\ \\ \\ \\ C: \\ Arquivo morto de scripts como o \\ nome completo da pasta. Passar apenas o nome da pasta – Arquivo Morto – resulta em um erro de caminho inválido.

A classe Diretório Win32 \_ não fornece um método de uma etapa para mover pastas. Em vez disso, mover uma pasta geralmente envolve duas etapas:

<dl> 1. Copiando a pasta para seu novo local  
2. Excluindo a pasta original  
</dl>

A única exceção para esse processo de duas etapas envolve mover uma pasta para um novo local na mesma unidade. Por exemplo, suponha que você queira mover C: \\ Temp para C: \\ Scripts de arquivos \\ \\ temporários. Desde que o local atual e o novo local estão na mesma unidade, você pode mover a pasta simplesmente chamando o método Renomear e passando o novo local como o parâmetro de método. Essa abordagem permite efetivamente que você mova a pasta em uma única etapa. No entanto, o script falhará se a unidade atual e a nova unidade são diferentes. Uma tentativa de renomear C: \\ Temp para D: \\ Temp falha com um erro "Unidade não é a mesma".

## <a name="examples"></a>Exemplos

O código a seguir, da amostra Mover uma Pasta Usando O VBScript do [WMI](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) na Galeria do TechNet, usa o método Renomear para mover a pasta C: Scripts para \\ C: Documentos administradores Arquivo \\ \\ \\ \\ VBScript.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery _ 
    ("Select * from Win32_Directory where name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults = objFolder.Rename("C:\Admins\Documents\Archive\VBScript") 
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
</dt> </dl>

 

