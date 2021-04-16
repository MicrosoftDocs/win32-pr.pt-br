---
description: A tabela a seguir descreve \_ as opções de soquete sol IRLMP que se aplicam aos soquetes criados para a família de endereços IrDA (Associação de dados de infravermelho) \_ e o IRLMP (protocolo de gerenciamento de link de infravermelho).
ms.assetid: 0457159d-8509-435c-8f57-752530d5df65
title: Opções de soquete de SOL_IRLMP (AF \_ IrDA. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090193aec00eaebd87494afefbafc7b1450fdb44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768276"
---
# <a name="sol_irlmp-socket-options"></a>\_Opções de soquete sol IRLMP

A tabela a seguir descreve as opções de soquete **sol \_ IRLMP** que se aplicam aos soquetes criados para a família de endereços IrDA (Associação de dados de infravermelho) \_ e o IRLMP (protocolo de gerenciamento de link de infravermelho). Consulte as páginas de referência de função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obter mais informações sobre como obter e definir opções de soquete.

Para enumerar protocolos e descobrir Propriedades com suporte para cada protocolo instalado, use a função [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

<dl> <dt><span id="SOL_IRLMP_Socket_Options"></span><span id="sol_irlmp_socket_options"></span><span id="SOL_IRLMP_SOCKET_OPTIONS"></span>**\_Opções de soquete sol IRLMP**</dt> <dd> <dl> <dt> 

| Opção                 | Obter | Definir | Tipo de optval     | Descrição                                                            |
|------------------------|-----|-----|-----------------|------------------------------------------------------------------------|
| \_modo de descoberta do IRLMP \_ |     |     |                 |                                                                        |
| IRLMP \_ ENUMDEVICES     | sim |     | **DEVICELIST**  | Retorna uma lista de IDs de dispositivo IrDA para dispositivos com capacidade de IR dentro do intervalo. |
| IRLMP \_ \_ modo exclusivo |     |     | DWORD (booliano) | Define o soquete para ignorar a camada TinyTP para se comunicar diretamente com IrLMP. |
| consulta do IRLMP \_ ias \_      | sim |     | **consulta do IAS \_**  | Consulta o IAS em um determinado serviço e nome de classe para seus atributos.      |
| IRLMP \_ conjunto de ias \_        |     | sim | **conjunto de IAS \_**    | Define um valor de atributo para um determinado nome de classe e atributo no IAS. |
| \_modo de IRLPT IRLMP \_     |     | sim | DWORD (booliano) | Habilita a comunicação com impressoras compatíveis com o IR.                        |
| parâmetros de IRLMP \_      |     |     |                 |                                                                        |
| \_Len de \_ PDU de envio IRLMP \_  | sim |     | DWORD           | Recupera o comprimento máximo de PDU necessário para usar \_ o \_ modo IRLMP 9WIRE.   |
| IRLMP \_ \_ modo nítido     |     | sim |                 |                                                                        |
| \_modo de TINYTP IRLMP \_    |     | sim |                 |                                                                        |
| \_Modo de 9WIRE IRLMP \_     | sim | sim | DWORD (booliano) | Coloca o Soquete IrDA no modo IrCOMM.                                 |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_SOL_IRLMP_options"></span><span id="windows_support_for_sol_irlmp_options"></span><span id="WINDOWS_SUPPORT_FOR_SOL_IRLMP_OPTIONS"></span>**Suporte do Windows para \_ Opções de sol IRLMP**</dt> <dd> <dl> <dt> 

| Opção                            | Windows 7 | Windows Server 2008 | Windows Vista | Windows Server 2003 | Windows XP | Windows 2000 | Windows me, Windows 98 | Windows NT 4.0 |
|-----------------------------------|-----------|---------------------|---------------|---------------------|------------|--------------|------------------------|----------------|
| \_modo de descoberta do IRLMP \_<br/> |           |                     |               |                     |            |              | x                      |                |
| IRLMP \_ ENUMDEVICES<br/>     | x         | x                   | x             | x                   | x          | x            | x                      |                |
| IRLMP \_ \_ modo exclusivo<br/> |           |                     |               |                     |            |              |                        |                |
| consulta do IRLMP \_ ias \_<br/>      | x         | x                   | x             | x                   | x          | x            | x                      |                |
| IRLMP \_ conjunto de ias \_<br/>        | x         | x                   | x             | x                   | x          | x            | x                      |                |
| \_modo de IRLPT IRLMP \_<br/>     | x         | x                   | x             | x                   | x          | x            |                        |                |
| parâmetros de IRLMP \_<br/>      |           |                     |               |                     |            |              | x                      |                |
| \_Len de \_ PDU de envio IRLMP \_<br/>  | x         | x                   | x             | x                   | x          | x            |                        |                |
| IRLMP \_ \_ modo nítido<br/>     |           |                     |               |                     |            |              |                        |                |
| \_modo de TINYTP IRLMP \_<br/>    |           |                     |               |                     |            |              | x                      |                |
| \_Modo de 9WIRE IRLMP \_<br/>     | x         | x                   | x             | x                   | x          | x            |                        |                |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

As opções de soquete **sol \_ IRLMP** e as estruturas usadas por essas opções de soquete são definidas no arquivo de cabeçalho *\_ IrDA. h de AF* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>\_IrDA. h de AF</dt> </dl> |



 

 




