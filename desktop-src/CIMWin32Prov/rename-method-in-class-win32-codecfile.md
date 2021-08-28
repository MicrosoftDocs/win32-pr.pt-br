---
description: Renomeia o arquivo codec especificado no caminho do objeto.
ms.assetid: fd6ce02c-d513-4643-ac27-313c32732f1e
ms.tgt_platform: multiple
title: Renomear o método da Win32_CodecFile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c1054ffe0c016c5e06159a13cbdf68d5cfa7521e96727867a74d25a635888165
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077456"
---
# <a name="rename-method-of-the-win32_codecfile-class"></a>Renomear o método da classe \_ CodecFile win32

O **método renomear** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) renomeia o arquivo codec especificado no caminho do objeto. Não há suporte para renomeação se o destino estiver em outra unidade ou se for necessário sobrescrever um arquivo lógico existente.

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

Retornará um valor inteiro de 0 (zero) se o arquivo tiver sido renomeado com êxito e qualquer outro número para indicar um erro.

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

[**CodecFile do Win32 \_**](win32-codecfile.md)
</dt> </dl>

 

