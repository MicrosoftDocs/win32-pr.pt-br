---
description: Obtém a propriedade do arquivo codec lógico especificado no caminho do objeto. Esse método é uma versão estendida do método TakeOwnerShip.
ms.assetid: 8f3b495a-f654-4818-b0ea-dc88819d72af
ms.tgt_platform: multiple
title: Método TakeOwnerShipEx da Win32_CodecFile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 04af6ed0953f25c5b02e988569eecad806ae62cb4757463831132e3c22dd40b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119546636"
---
# <a name="takeownershipex-method-of-the-win32_codecfile-class"></a>Método TakeOwnerShipEx da classe CodecFile Win32 \_

O método de classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShipEx** obtém a propriedade do arquivo codec lógico especificado no caminho do objeto. Esse método é uma versão estendida do [**método TakeOwnerShip.**](takeownership-method-in-class-win32-directory.md) Se o arquivo lógico for realmente um diretório, esse método atuará recursivamente, assumindo a propriedade de todos os arquivos e subdiretivos que o diretório contém.

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Nome do arquivo ou diretório em que o **método TakeOwnerShipEx** falhou. Esse parâmetro será **NULL se** o método for bem-sucedido.

</dd> <dt>

*StartFileName* \[ in, opcional\]
</dt> <dd>

Nomeia o arquivo ou diretório filho a ser usado como um ponto de partida **para TakeOwnerShipEx.** O *parâmetro StartFileName* normalmente é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada de método anterior. Se esse parâmetro for **NULL,** a operação será executada no arquivo ou diretório especificado na **chamada ExecMethod.**

</dd> <dt>

*Recursivo* \[ in, opcional\]
</dt> <dd>

Se **true**, a alteração de propriedade será aplicada recursivamente a arquivos e diretórios dentro do diretório especificado pela [**instância de \_ LogicalFile cim.**](cim-logicalfile.md) Observação: para instâncias de arquivo, o *parâmetro de entrada recursiva* é ignorado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor inteiro de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.

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

 

