---
description: Altera o estado do trabalho.
ms.assetid: 3B11CE45-63E4-43D1-AAF6-02F83C9CBB85
title: 'Método Msvm_CopyFileToGuestJob:: RequestStateChange'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 09fdc3a1ee7d0f8942e1e02c5d18f20c42f74db2e65ae065132f164b199ee861
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014334"
---
# <a name="msvm_copyfiletoguestjobrequeststatechange-method"></a>\_Método Msvm CopyFileToGuestJob:: RequestStateChange

Altera o estado do trabalho.

## <a name="syntax"></a>Sintaxe


```C++
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Requestedstate* \[ no\]
</dt> <dd>

O novo estado. Estes são os valores possíveis:

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**Início** (2)


</dt> <dd>

Altera o estado para ' running '.

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**Suspender** (3)


</dt> <dd>

Interrompe o trabalho temporariamente. O cliente pode, então, reiniciar o trabalho posteriormente com ' Start '. O cliente pode, possivelmente, inserir o estado ' serviço ' enquanto estiver suspenso (isso é específico do trabalho).

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminar** (4)


</dt> <dd>

Interrompe o trabalho corretamente, salvando os dados, preservando o estado e desligando todos os processos subjacentes de maneira ordenada.

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**Kill** (5)


</dt> <dd>

Encerra o trabalho imediatamente sem nenhum requisito para salvar dados ou preservar o estado.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Serviço** (6)


</dt> <dd>

Coloca o trabalho em um estado de serviço específico do fornecedor. O cliente pode possivelmente reiniciar o trabalho.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (7.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*TimeoutPeriod* \[ no\]
</dt> <dd>

Um período de tempo limite que especifica a quantidade máxima de tempo que o cliente espera que a transição para o novo Estado tenha. O formato do intervalo deve ser usado para especificar o período de tempo limite. Um valor 0 ou **NULL** indica que o cliente não tem requisitos de tempo para a transição. Se essa propriedade não contiver 0 ou **NULL** e a implementação não oferecer suporte a esse parâmetro, um código de retorno 4098 (**uso do parâmetro timeout sem suporte**) deverá ser retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos valores a seguir.



| Código/valor de retorno                                                                                                                                                               | Descrição                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**Concluído sem erro**</dt> <dt>0</dt> </dl>                   | Êxito.<br/>                                                                |
| <dl> <dt>**Uso do parâmetro timeout sem suporte**</dt> <dt>4098</dt> </dl> |                                                                                    |
| <dl> <dt>32768</dt> <dt>**com falha**</dt> </dl>                                |                                                                                    |
| <dl> <dt>**Acesso negado**</dt> <dt>32769</dt> </dl>                         | Acesso negado<br/>                                                          |
| <dl> <dt>**Sem suporte**</dt> <dt>32770</dt> </dl>                         |                                                                                    |
| <dl> O <dt>**status é desconhecido**</dt> <dt>32771</dt> </dl>                     |                                                                                    |
| <dl> <dt>**Tempo limite**</dt> <dt>32772</dt> </dl>                               |                                                                                    |
| <dl> <dt>**Parâmetro inválido**</dt> <dt>32773</dt> </dl>                     |                                                                                    |
| <dl> O <dt>**sistema está em uso**</dt> <dt>32774</dt> </dl>                      |                                                                                    |
| <dl> <dt>**Estado inválido para esta operação**</dt> <dt>32775</dt> </dl>      | Não há suporte para o valor especificado no parâmetro *requestedstate* .<br/> |
| <dl> <dt>**Tipo de dados incorreto**</dt> <dt>32776</dt> </dl>                   |                                                                                    |
| <dl> O <dt>**sistema não está disponível**</dt> <dt>32777</dt> </dl>               |                                                                                    |
| <dl> <dt>**Memória insuficiente**</dt> <dt>32778</dt> </dl>                         |                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                                                 |
| Namespace<br/>                | \\\\\\Virtualização \\ v2 de raiz<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




