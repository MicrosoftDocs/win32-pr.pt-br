---
description: Copia o arquivo de dispositivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo parâmetro FileName.
ms.assetid: 42cdb880-2431-4dcc-abdb-f271e2cd81a4
ms.tgt_platform: multiple
title: Método CopyEx da classe CIM_DeviceFile dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 859687d879a73b78531e86a4f7306bc8f943de668005bc2bf5d8a99d0731f168
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003886"
---
# <a name="copyex-method-of-the-cim_devicefile-class"></a>Método CopyEx da classe \_ DeviceFile CIM

O **método CopyEx** copia o arquivo de dispositivo lógico (ou diretório) especificado no caminho do objeto para o local especificado pelo *parâmetro FileName.* Não há suporte para uma cópia se a substituição de um arquivo lógico existente for necessária. Esse método é uma versão estendida do [**método Copy.**](copy-method-in-class-cim-devicefile.md) Esse método é herdado de [**CIM \_ LogicalFile.**](cim-logicalfile.md)

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 CopyEx(
  [in]  string     FileName,
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FileName* \[ Em\]
</dt> <dd>

Nome totalmente qualificado do arquivo de destino (ou diretório).

Exemplo: "c: \\ temp \\ newdirectory"

</dd> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou. Esse parâmetro será **nulo** se o método for bem-sucedido.

</dd> <dt>

*StartFileName* \[ Em\]
</dt> <dd>

Cadeia de caracteres que representa o arquivo filho (ou diretório) a ser usado como um ponto de partida para esse método. Normalmente, o *parâmetro StartFileName* é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada de método anterior. Se esse parâmetro for **nulo,** a operação será executada no arquivo (ou diretório) especificado na [**chamada ExecMethod.**](/windows/desktop/WmiSdk/swbemservices-execmethod)

</dd> <dt>

*Recursivo* \[ Em\]
</dt> <dd>

Se TRUE, o método também será aplicado recursivamente a arquivos e diretórios dentro do diretório especificado pela [**instância \_ de DeviceFile cim.**](cim-devicefile.md) Para instâncias de arquivo, esse parâmetro é ignorado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.

<dl> <dt>


</dt> <dd>

0

Sucesso.

</dd> <dt>


</dt> <dd>

2

Acesso negado

</dd> <dt>


</dt> <dd>

8

Falha não especificada.

</dd> <dt>


</dt> <dd>

9

Objeto inválido.

</dd> <dt>


</dt> <dd>

10

O objeto já existe.

</dd> <dt>


</dt> <dd>

11

Sistema de arquivos não NTFS.

</dd> <dt>


</dt> <dd>

12

Plataforma não Windows.

</dd> <dt>


</dt> <dd>

13

A unidade não é a mesma.

</dd> <dt>


</dt> <dd>

14

O diretório não está vazio.

</dd> <dt>


</dt> <dd>

15

Violação de compartilhamento.

</dd> <dt>


</dt> <dd>

16

Arquivo inicial inválido.

</dd> <dt>


</dt> <dd>

17

Privilégio não mantido.

</dd> <dt>


</dt> <dd>

21

Parâmetro inválido.

</dd> </dl>

## <a name="remarks"></a>Comentários

Atualmente, esse método não é implementado pelo WMI. Para usar esse método, você deve implementá-lo em seu próprio provedor.

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

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

[CIM \_ DeviceFile](copyex-method-in-class-cim-devicefile.md)
</dt> <dt>

[**CIM \_ DeviceFile**](cim-devicefile.md)
</dt> </dl>

 

