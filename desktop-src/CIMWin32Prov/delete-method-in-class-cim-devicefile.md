---
description: Método Delete da classe CIM_DeviceFile – o método Delete exclui o arquivo lógico (ou diretório) especificado no caminho do objeto. Esse método é herdado do \_ LogicalFile CIM.
ms.assetid: 490d0578-a545-423b-9640-ec09f4ef8d96
ms.tgt_platform: multiple
title: Método Delete da classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e96ba9837252158510c306a622df86c09bbfd96
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089624"
---
# <a name="delete-method-of-the-cim_devicefile-class"></a>Método Delete da classe CIM \_ devicefile

O método **delete** exclui o arquivo lógico (ou diretório) especificado no caminho do objeto. Esse método é herdado [**do \_ LogicalFile CIM**](cim-logicalfile.md).

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 Delete();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.

<dl> <dt>

**0**
</dt> <dd>

Sucesso.

</dd> <dt>

**2**
</dt> <dd>

Acesso negado.

</dd> <dt>

**8**
</dt> <dd>

Falha não especificada.

</dd> <dt>

**9**
</dt> <dd>

Objeto inválido.

</dd> <dt>

**10**
</dt> <dd>

O objeto já existe.

</dd> <dt>

**11**
</dt> <dd>

Sistema de arquivos não NTFS.

</dd> <dt>

**12**
</dt> <dd>

Plataforma não Windows.

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

Violação de compartilhamento.

</dd> <dt>

**16**
</dt> <dd>

Arquivo inicial inválido.

</dd> <dt>

**17**
</dt> <dd>

Privilégio não mantido.

</dd> <dt>

**Abril**
</dt> <dd>

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

[\_Dispositivo CIM](delete-method-in-class-cim-devicefile.md)
</dt> <dt>

[**\_Dispositivo CIM**](cim-devicefile.md)
</dt> </dl>

 

