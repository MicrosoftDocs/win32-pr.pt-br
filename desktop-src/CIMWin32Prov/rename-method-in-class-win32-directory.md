---
description: Renomeia o arquivo de entrada de diretório especificado no caminho do objeto.
ms.assetid: 8bfe1b69-5f93-4408-a742-f03a9cb16bfe
ms.tgt_platform: multiple
title: Método Rename da classe Win32_Directory
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
ms.openlocfilehash: 874151e1ff8c9feca375df3eb441665863d1070d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753583"
---
# <a name="rename-method-of-the-win32_directory-class"></a>Método Rename da classe do \_ diretório Win32

O método **renomear** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) renomeia o arquivo de entrada de diretório especificado no caminho do objeto. Não haverá suporte para renomear se o destino estiver em outra unidade ou se for necessário substituir um arquivo lógico existente.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

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

Novo nome totalmente qualificado do arquivo (ou diretório). Exemplo: c: \\ temp \\newfile.txt.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de 0 (zero) se o arquivo tiver sido renomeado com êxito e qualquer outro número para indicar um erro.

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

Para renomear uma pasta, primeiro associe-se à pasta em questão e, em seguida, chame o método Rename. Como o único parâmetro para o método, passe o novo nome da pasta como um nome de caminho completo. Por exemplo, se a pasta no backup de logs de scripts C: \\ \\ \\ for renomeada como c: \\ script \\ arquivo, você deverá passar \\ o arquivo c: scripts \\ como o nome de pasta completo. Passar somente o nome da pasta-arquivo-resulta em um erro de caminho inválido.

A classe de diretório Win32 não \_ fornece um método de uma etapa para mover pastas. Em vez disso, mover uma pasta geralmente envolve duas etapas:

<dl> 1. Copiando a pasta para seu novo local  
2. Excluindo a pasta original  
</dl>

A única exceção para esse processo de duas etapas envolve mover uma pasta para um novo local na mesma unidade. Por exemplo, suponha que você deseja mover C: \\ Temp para c: \\ scripts \\ arquivos temporários \\ arquivo morto. Desde que o local atual e o novo local estejam na mesma unidade, você pode mover a pasta simplesmente chamando o método Rename e passando o novo local como o parâmetro Method. Essa abordagem permite efetivamente que você mova a pasta em uma única etapa. No entanto, o script falhará se a unidade atual e a nova unidade forem diferentes. Uma tentativa de Renomear C: \\ Temp para D: \\ Temp falha com um erro "a unidade não é o mesmo".

## <a name="examples"></a>Exemplos

O código a seguir, a partir da amostra [mover uma pasta usando o WMI](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) VBScript na galeria do TechNet, usa o método Rename para mover a pasta c: \\ scripts para C: \\ Admins \\ documentam o \\ \\ VBScript.


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
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Diretório Win32**](win32-directory.md)
</dt> </dl>

 

