---
description: Exclua o arquivo de codec de áudio lógico ou vídeo (ou diretório) especificado no caminho do objeto.
ms.assetid: df85c8a4-3be3-4bde-b36e-6bc8af6495a9
ms.tgt_platform: multiple
title: Método DeleteEx da Win32_CodecFile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f749455a15e92427f4f0fec50abce7ea8ba83b44f9244b3b61208fb27dd12b9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077666"
---
# <a name="deleteex-method-of-the-win32_codecfile-class"></a>Método DeleteEx da classe \_ CodecFile win32

O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **DeleteEx** excluirá o arquivo de codec de áudio lógico ou vídeo especificado no caminho do objeto. **DeleteEx** é uma versão estendida do [**método Delete.**](delete-method-in-class-win32-directory.md)

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 DeleteEx(
  [out] string StopFileName,
  [in]  String StartFileName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Nome do arquivo ou diretório em que o **método DeleteEx** falhou. Esse parâmetro será **nulo se** o método for bem-sucedido.

</dd> <dt>

*StartFileName* \[ Em\]
</dt> <dd>

Nomeia o arquivo ou diretório filho a ser usado como um ponto de partida **para DeleteEx.** O *parâmetro StartFileName* normalmente é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada de método anterior. Se esse parâmetro for **NULL,** a operação será executada no arquivo ou diretório especificado na **chamada ExecMethod.** Esse parâmetro é opcional.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará um valor inteiro de 0 (zero) se o arquivo tiver sido excluído com êxito e qualquer outro número para indicar um erro.

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

 

