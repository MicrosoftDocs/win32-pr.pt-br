---
description: Verifica se o chassi físico referenciado pode ser contido ou inserido no pacote físico.
ms.assetid: 9a1aa1b7-2b95-4887-9d14-e416ff69f9df
ms.tgt_platform: multiple
title: Método iscompatível da classe CIM_Chassis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chassis.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8796582b153a7283429715569eeed91e4dd38fc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754820"
---
# <a name="iscompatible-method-of-the-cim_chassis-class"></a>Método iscompatível da classe de \_ chassi CIM

O método **iscompatível** verifica se o chassi físico referenciado pode ser contido ou inserido no pacote físico. Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado usando um qualificador [**ValueMap**](/windows/desktop/WmiSdk/standard-qualifiers) no método. As cadeias de caracteres nas quais os conteúdos de **ValueMap** são convertidos também podem ser especificadas na subclasse como um qualificador de matriz de **valores** . Esse método é herdado do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ElementToCheck* \[ no\]
</dt> <dd>

Referência ao elemento físico para o qual verificar a compatibilidade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de 0 (zero) em caso de sucesso, 1 (um) se a solicitação não tiver suporte e qualquer outro número para indicar um erro.

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Chassi CIM**](iscompatible-method-in-class-cim-chassis.md)
</dt> <dt>

[**\_Chassi CIM**](cim-chassis.md)
</dt> </dl>

 

