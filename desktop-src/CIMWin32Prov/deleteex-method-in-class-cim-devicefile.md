---
description: Método DeleteEx da classe CIM_DeviceFile – o método DeleteEx exclui o arquivo lógico (ou diretório) especificado no caminho do objeto. Esse método é uma versão estendida do método Delete e é herdado de CIM \_ LogicalFile.
ms.assetid: ef4d08cd-7287-47be-bcfc-edc248ac5c9b
ms.tgt_platform: multiple
title: Método DeleteEx da classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f9d7c54c08e6709d06a46b519dd1b9c8d51daf2b6862c5f59a93c9a0a97d2ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118676582"
---
# <a name="deleteex-method-of-the-cim_devicefile-class"></a>Método DeleteEx da classe CIM \_ devicefile

O método **DeleteEx** exclui o arquivo lógico (ou diretório) especificado no caminho do objeto. Esse método é uma versão estendida do método [**delete**](delete-method-in-class-cim-devicefile.md) e é herdado de [**CIM \_ LogicalFile**](cim-logicalfile.md).

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*StopFileName* \[ fora\]
</dt> <dd>

Cadeia de caracteres que representa o nome do arquivo (ou diretório) em que o método falhou. Esse parâmetro será nulo se o método tiver sucesso.

</dd> <dt>

*StartFileName* \[ no\]
</dt> <dd>

Cadeia de caracteres que representa o arquivo filho (ou diretório) a ser usado como ponto de partida para esse método. Normalmente, o parâmetro **StartFileName** é o parâmetro **StopFileName** que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior. Se esse parâmetro for nulo, a operação será executada no arquivo ou diretório especificado na chamada de [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .

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

Acesso negado.

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

Este método não está implementado no momento pelo WMI. Para usar esse método, você deve implementá-lo em seu próprio provedor.

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[\_Dispositivo CIM](deleteex-method-in-class-cim-devicefile.md)
</dt> <dt>

[**\_Dispositivo CIM**](cim-devicefile.md)
</dt> </dl>

 

