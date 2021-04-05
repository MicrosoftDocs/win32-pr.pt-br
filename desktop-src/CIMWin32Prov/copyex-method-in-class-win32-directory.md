---
description: Copia o arquivo de entrada de diretório lógico ou o diretório especificado no caminho do objeto para o local especificado pelo parâmetro FileName. Esse método é uma versão estendida do método Copy.
ms.assetid: c15bd1ae-a60d-4875-a76e-99486820c42c
ms.tgt_platform: multiple
title: Método CopyEx da classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55f2fdb0aa4e8306e8ec0aa4f5f265c0a8ee6689
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826708"
---
# <a name="copyex-method-of-the-win32_directory-class"></a>Método CopyEx da classe do \_ diretório Win32

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CopyEx** copia o arquivo de entrada de diretório lógico ou o diretório especificado no caminho do objeto para o local especificado pelo parâmetro *filename* . Esse método é uma versão estendida do método [**Copy**](copy-method-in-class-win32-directory.md) . Não haverá suporte para uma cópia se a substituição de um arquivo lógico existente for necessária.

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome do arquivo* \[ no\]
</dt> <dd>

Nome totalmente qualificado da cópia do arquivo (ou diretório). Exemplo: c: \\ temp \\ newdirectory.

</dd> <dt>

*StopFileName* \[ fora\]
</dt> <dd>

Nome do arquivo ou diretório em que o método **CopyEx** falhou. Esse parâmetro será **NULL** se o método tiver sucesso.

</dd> <dt>

*StartFileName* \[ em, opcional\]
</dt> <dd>

Nomeia o arquivo ou diretório filho a ser usado como ponto de partida para **CopyEx**. O parâmetro *StartFileName* normalmente é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior. Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de **ExecMethod** .

Se o *StartFileName* for usado, *recursivo* deverá ser definido como true também.

</dd> <dt>

*Recursivo* \[ em, opcional\]
</dt> <dd>

Se **for true**, os arquivos e diretórios serão copiados recursivamente dentro do diretório especificado pela instância de [**\_ LogicalFile do CIM**](cim-logicalfile.md) .

> [!Note]  
> Para instâncias de arquivo, o parâmetro de entrada *recursivo* é ignorado.

 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

 

