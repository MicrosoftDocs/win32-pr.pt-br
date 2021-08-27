---
description: Embora haja poucos limites técnicos para o tipo e o tamanho dos dados que um aplicativo pode armazenar no registro, algumas diretrizes práticas existem para promover a eficiência do sistema.
ms.assetid: fa85ff87-3d72-4f71-856a-f43df7d19aa8
title: espaço de Armazenamento do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00414edbd34452fd6943a4d73a2ebe85af5d38884ddd0ca77f1d8fb41ae6e0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885074"
---
# <a name="registry-storage-space"></a>espaço de Armazenamento do registro

Embora haja poucos limites técnicos para o tipo e o tamanho dos dados que um aplicativo pode armazenar no registro, algumas diretrizes práticas existem para promover a eficiência do sistema. Um aplicativo deve armazenar dados de configuração e inicialização no registro e armazenar outros tipos de dados em outro lugar.

Em geral, os dados que consistem em mais de um ou dois kilobytes (K) devem ser armazenados como um arquivo e referenciados usando uma chave no registro em vez de serem armazenados como um valor. Em vez de duplicar grandes partes de dados no registro, um aplicativo deve salvar os dados como um arquivo e fazer referência ao arquivo. O código binário executável nunca deve ser armazenado no registro.

Uma entrada de valor usa muito menos espaço do registro do que uma chave. Para economizar espaço, um aplicativo deve agrupar dados semelhantes como uma estrutura e armazenar a estrutura como um valor, em vez de armazenar cada um dos membros da estrutura como uma chave separada. (Armazenar os dados em formato binário permite que um aplicativo armazene dados em um valor que, de outra forma, seria composto de vários tipos incompatíveis.)

As exibições dos arquivos do registro são mapeadas na memória do pool paginável.

**Windows server 2008 para 32 bits, Windows vista com SP1 para 32-bit, Windows Vista, Windows Server 2003, Windows XP:** As exibições dos arquivos de registro são mapeadas no espaço de endereço de cache do computador. Portanto, independentemente do tamanho dos dados do registro, não é cobrado mais de 4 megabytes (MB).

O tamanho máximo de um hive de registro é 2 GB, exceto o hive do sistema.

**Windows server 2003 com SP1, Windows server 2003 e Windows XP:** Não há limites explícitos na quantidade total de espaço que pode ser consumida por Hives na memória do pool paginável e no espaço em disco, embora as cotas do sistema possam afetar o tamanho máximo real. o tamanho máximo de um hive do registro foi limitado a 2 GB a partir do Windows Server 2003 com Service Pack 2 (SP2).

O tamanho máximo do hive do sistema é limitado pela memória física, conforme mostrado na tabela a seguir. 

| Sistema                      | Tamanho máximo do hive do sistema                                                                                                                                                                                                            |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sistemas baseados em x86           | 50 por cento da memória física, até 400 MB. **Windows server 2003 com SP2, Windows server 2003 com SP1, Windows Server 2003 e Windows XP:** 25% da memória física, até 200 MB.<br/>                                    |
| sistemas baseados em x64           | 50 por cento da memória física, até 1,5 GB. **Windows Server 2003 com SP2:** 25% da memória do sistema, até 200 MB.<br/> **Windows server 2003 com SP1, Windows server 2003 e Windows XP 64-Bit Edition:** 32 MB.<br/> |
| Sistemas Intel baseados em Itanium | 50 por cento da memória física, até 1 GB. **Windows server 2008, Windows Vista, Windows server 2003 com SP2, Windows server 2003 com SP1, Windows server 2003 e Windows XP 64-Bit Edition:** 32 MB.<br/>                         |



 

## <a name="windows-2000"></a>Windows 2000

Os dados do registro são armazenados no pool paginável, uma área de memória física usada para dados do sistema que podem ser gravados no disco quando não estão em uso. O valor **RegistrySizeLimit** estabelece a quantidade máxima de pool paginável que pode ser consumida por dados de registro de todos os aplicativos. Esse valor está localizado na seguinte chave do registro:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
```

Por padrão, o limite de tamanho do registro é 25 por cento do pool paginado. (O tamanho padrão do pool paginado é de 32 MB, portanto, é 8 MB.) O sistema garante que o valor mínimo de **RegistrySizeLimit** seja 4 MB e o máximo seja aproximadamente 80% do valor de **PagedPoolSize** . Se o valor dessa entrada for maior que 80% do tamanho do pool paginado, o sistema definirá o tamanho máximo do registro como 80% do tamanho do pool paginado. Isso impede que o registro consuma espaço necessário pelos processos. Observe que a definição desse valor não aloca espaço no pool paginável, nem garante que o espaço estará disponível, se necessário.

O tamanho do pool paginado é determinado pelo valor de **PagedPoolSize** na seguinte chave do registro:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            SessionManager
               MemoryManagement
```

Para obter um exemplo de como determinar os tamanhos atuais e máximos do registro, consulte [determinando o tamanho do registro](determining-the-registry-size.md).

O pool de páginas máximos é de aproximadamente 300.470 MB, portanto, o limite de tamanho do registro é de 240-376 MB. No entanto, se a opção/3GB for usada, o tamanho máximo de pool paginado será de 192 MB, de modo que o registro pode ter um máximo de 153,6 MB.

 

 




